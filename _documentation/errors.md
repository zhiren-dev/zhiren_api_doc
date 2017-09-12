---
title: 错误码
position: 4
right_code: |
  ~~~ json
  {
    "code": 1xxx,
    "text": "error message here"
  }
  ~~~
  {: title="Response" }
---

正常API返回的 HTTP Status Code 为 2xx 或 3xx。如果遇到错误，HTTP Status Code 为 4xx 或 5xx,
同时返回报文内容会包含具体错误信息，包括错误代码和错误消息。

## API 错误代码列表

错误代码 | 描述
-------- | -------
**1xxx** | **认证错误**
1001     | 缺少 access_key
1002     | 缺少签名
1003     | 缺少 tonce
1101     | 签名无效
1102     | 不存在的记录
1103     | tonce 无效
1104     | 没有找到对应的公司
1105     | access_key 无效
**2xxx** | **参数错误**
2001     | 未实现：API参数验证错误
2002     | 对象验证错误
2003     | 未实现：无效的身份事项代码
2004     | JSON 格式错误
**3xxx** | **参数错误**
3001     | 没有权限访问该 API
3002     | bind_code 已过期
**9xxx** | **其他错误**
