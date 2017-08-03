# Oauth Authorization - 授权

知人为第三方服务进行标准 Oauth2 协议授权，允许操作用户数据，通过 API 请求用户数据前，需要实现进行授权，并取得授权 token。

对应的每个第三方服务，都有唯一的 `app_id` ，`app_secret`与
`callback_url`。
对应的每个第三方服务的每个用户，都有唯一的`response_code`， `access_token`。

参数名 | 描述
-------- | -------
**app_id** | 客户端访问识别码，当您成为知人第三方服务，对应每个开通服务的公司，都会有一对 app_id， app_secret 和 callback_url, 用于建立ouath请求，并且在用户进行授权请求中附上。
**callback_url**  | 用户授权后的回调 URL，用户授权后将跳转到该地址。 
**response_code**  | 用户授权后成功后，返回给第三方一个repsonse_code，用于标明是该用户已授权，此时，第三方将app_id，app_secret，callback_url以及response_code一同发送给知人，将返回唯一授权标识access_token。 
**access_token**  | 当用户在第三方请求知人服务时，附上 access_token = `access token value` 参数，即可调用知人 Oauth API。
