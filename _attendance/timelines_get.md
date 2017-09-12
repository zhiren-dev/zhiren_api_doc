---
title: 查询请假和公出
position: 6.4
type: get
---

**GET** `/api/v2/employees/:guid/timelines`
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
start_date | 开始日期   |        | 是   |
end_date   | 结束日期   |        | 是   |
category   | 字符串     |        | 是   | leave: 请假；business_trip: 公出

### Response

### Response
[Timeline 对象](#objecttimeline) 数组