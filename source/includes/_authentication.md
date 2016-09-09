# Authentication - 认证

通过 API 请求『知人』时，每一个需要验证的请求都要进行签名，签名需要用到 `access_key` 与 `secret_key`。

这里有一个概念需要说明一下。签名用于验证第三方发过来的请求, 比如 『访客』。我们将第三方称为『Product』。


参数名         | 描述
---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
**access_key** | 访问识别码，当你申请成为『访客』客户端，您会获得一对  access_key 和 secret_key, 其中 access_key 必须在每次请求中附上，以便于我们知道请求来自于您。而 secret_key 请务必放在私有的空间，千万不可在请求中传递。
**signature**  | 使用你的 secret_key 进行签名后的字符串， 具体签名的方法后面会进一步描述
**tonce**      | 请求时间, 必须以 [Unix Time](https://en.wikipedia.org/wiki/Unix_time) 的格式发送, tonce与服务器时间不得超过正负30秒, 否则请求将视为无效。
**payload**    | 被签名的数据体部分， 用 JSON 进行编码。

### 签名的算法

我们用伪代码表示签名的算法如下：

    **signature = HMAC-SHA256( secret_key, string_to_sign )**

首先根据请求的参数，把参数转换为 string_to_sign, 然后用 HMAC-SHA256 算法， 和你的 secret_key 进行签名。
所获得的签名结果必须在每次请求代入，并以 “signature” 为名作为参数， 我们将以此对你的请求合法性进行验证。

### string_to_sign 的生成方式

上面的公式中有一个string_to_sign， 这里我们详细谈谈它，string_to_sign 由五部分组成：

组成部分 | 描述
-------- | -------
**http_method** | 必须为大写， 比如 "POST", "GET", "DELETE", "PATCH" 等
**path** | 假设你请求的uri为 https://zhirenhr.com/api/v1/apple 那么 path 应该为 /api/v1/apple
**access_key** | 访问识别码
**tonce** | 请求时间
**payload** | 被签名的数据体部分， 用 JSON 进行编码。

那么最终用于签名的原字符串，就是把这五个部分链接起来皆可(注意顺序不可颠倒)：

```
    string_to_sign ＝ http_method + path + access_key + tonce + payload.to_json
    signature = OpenSSL::HMAC.hexdigest 'SHA256', secret_key, string_to_sign
```

```ruby
  ### 签名算法 Ruby 实现
  string_to_sign ＝ "#{http_method}#{path}#{access_key}#{tonce}#{payload.to_json}"
  OpenSSL::HMAC.hexdigest 'SHA256', secret_key, string_to_sign
```

然后将 signature，一并发送给服务器端即可（算法如右）
