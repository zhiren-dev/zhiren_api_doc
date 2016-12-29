# Introduction - 序言

欢迎使用知人的应用编程接口 API v2.0 通过 API 您可以接入知人提供的大部分服务。

知人 API v2.0 遵循 RESTful 风格，所有 API 的 URL 都是 `https://zhiren.com/api/v2/<apiname>`。

1. 请求中的业务数据以 JSON 格式传递，认证数据则以 URL 查询参数的形式传递。
2. 响应以 HTTP Status Code 来表示成功（2xx）或失败，如果失败，则会在响应体中以 JSON 格式给出详细的错误信息。
