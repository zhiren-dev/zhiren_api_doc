# Introduction

欢迎使用知人 API v2.0。通过 API 你可以在你自己的应用中接入知人提供的服务。

知人 API v2.0 遵循 RESTful 风格。

1. 请求中的业务数据以 JSON 格式传递，认证数据则以 URL 查询参数的形式传递。
2. 响应以 HTTP Status Code 来表示成功（2xx）或失败，如果失败，则会在响应体中以 JSON 格式给出详细的错误信息。

目前本系统只提供了 Ruby SDK。
