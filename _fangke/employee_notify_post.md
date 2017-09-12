---
title: 提醒员工接见访客
position: 10.2
type: post
---

**POST** `/api/v2/employees/:guid/notify`
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
token | 字符串 |        | 是   | 区别公司的标识符
name  | 字符串 |        | 是   | 访客姓名
time  | 字符串 |        | 是   | 到访时间

### Response

[员工对象](#objectemployee)