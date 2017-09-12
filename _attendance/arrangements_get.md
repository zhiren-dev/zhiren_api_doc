---
title: 查询员工排班
position: 6.3
type: get
---

**GET** `/api/v2/arrangement_employees`
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
empnoes | 列表 |        | 是   | 员工工号列表，例如：['1001', '1002', '1003']
start_date | 字符串 |        | 是   | 查询开始日期
end_date | 字符串 |        | 是   | 查询结束日期

### Response
[排班对象](#objectarrangement) 数组