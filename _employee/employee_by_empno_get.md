---
title: 按工号查询员工
position: 5.2
type: get

---

**GET** `/api/v2/employees/:empno`
{: .success }

empno
: 员工工号

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


### Response

JSON 格式的 [员工对象](#objectemployee)
