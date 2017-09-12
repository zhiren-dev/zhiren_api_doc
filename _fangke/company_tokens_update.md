---
title: 更新公司令牌
position: 10.1
type: patch
---

**PATCH** `/api/v2/company_tokens/:guid`
{: .success }



### HTTP Parameters

参数       | 类型       | 默认值 | 必须 | 描述
-----------|------------|--------|------|----------------------------|
payload    | JSON字符串 |        | 是   | JSON Payload
access_key | 字符串     |        | 是   | API Key
tonce      | 整型       |        | 是   | 以秒为单位的UNIX timestamp
signature  | 字符串     |        | 是   | 请求签名

**Payload Schema**

属性  | 类型   | 默认值 | 必须 | 描述
------|--------|--------|------|-------------------|
token | 字符串 |        | 是   | 区别
zhiren_visitor_token | 字符串 |        | 是   | fangke 提供给 zhiren 的令牌