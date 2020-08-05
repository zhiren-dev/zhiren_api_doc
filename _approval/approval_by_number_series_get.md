---
title: 按审批单号查询审批
position: 12.2
type: get

---

**GET** `/api/v2/approvals/:number_series`
{: .success }

number_series
: 审批单号

### HTTP Parameters

参数       | 类型       | 默认值 | 必须 | 描述
-----------|------------|--------|------|----------------------------|
payload    | JSON字符串 |        | 是   | JSON Payload
access_key | 字符串     |        | 是   | API Key
tonce      | 整型       |        | 是   | 以秒为单位的UNIX timestamp
signature  | 字符串     |        | 是   | 请求签名


### Response

JSON 格式的 [审批对象](#objectapproval)
