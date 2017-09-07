---
title: 认证
position: 2
right_code: |
  ~~~ javascript
  $.get("https://zhiren.com/api/v2/employees", {
    "access_key": "YOUR_APP_KEY",
    "signature": "YOUR_SIGNATURE",
    "tonce": "YOUR_TONCE",
    "payload": "YOUR_PAYLOAD"
  }, function(data) {
    alert(data);
  });
  ~~~
  {: title="jQuery" }

  ~~~ bash
  curl "https://zhiren.com/api/v2/employees?access_key=YOUR_APP_KEY&\
  signature=YOUR_SIGNATURE&\
  tonce=YOUR_TONCE&\
  payload=YOUR_PAYLOAD"
  ~~~
  {: title="Curl" }
---
知人第三方服务称为 Product，通过 API 请求知人时，每一个需要验证的请求都要进行签名。

Product 对应每个 Company 都有唯一的 `access_key` 与 `secret_key` 。

access_key
: 访问识别码，当您成为知人第三方服务，对应每个开通服务的公司，都会有一对 access_key 和 secret_key, 其中 access_key 必须在每次请求中附上，而 secret_key 请务必放在私有的空间，千万不可在请求中传递。

signature
: 使用你的 secret_key 进行签名后的字符串，放入 header 的自定义字段 x-zhiren-signature

tonce
: 请求时间, 必须以 [Unix Time](https://en.wikipedia.org/wiki/Unix_time) 的格式发送, tonce与服务器时间不得超过正负 5 分钟, 否则请求将视为无效。

payload
: 被签名的数据体部分，JSON 格式的字符串。


### signature 的算法

我们用伪代码表示签名的算法如下：

**signature = HMAC-SHA256( secret_key, string_to_sign )**
{: .info }

首先根据请求的参数，把参数转换为 string_to_sign, 然后用 HMAC-SHA256 算法和你的 secret_key 进行签名。

### string_to_sign 的生成方式
上面的公式中的 string_to_sign 由五部分组成：

~~~ ruby
  string_to_sign = http_method + path + access_key + tonce + payload.to_json
  signature = OpenSSL::HMAC.hexdigest 'SHA256', secret_key, string_to_sign
~~~
{: title="Ruby" }

~~~ javascript
var utf8 = require("utf8");
var crypto = require("crypto");
signature = crypto.createHmac('sha256', secret_key).update(utf8.encode(payload_str)).digest('hex');
~~~
{: title="Javascript" }

组成部分 | 描述
-------- | -------
**http_method** | 必须为大写， 比如 "POST", "GET", "DELETE", "PATCH" 等
**path** | 假设你请求的uri为 https://zhiren.com/api/v2/example 那么 path 应该为 /api/v2/example
**access_key** | 访问识别码
**tonce** | 请求时间
**payload** | 被签名的数据体部分，JSON 格式的字符串。


那么最终用于签名的原字符串，就是把这五个部分链接起来皆可（注意顺序不可颠倒）。
