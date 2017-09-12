---
title: 查询分公司员工
position: 3.3
type: get
---

**GET** `/api/v2/sub_companies/:sub_company_uuid/employees`
{: .success }

sub_company_uuid
: 分公司 uuid

### HTTP Parameters

参数       | 类型       | 默认值 | 必须 | 描述
-----------|------------|--------|------|----------------------------|
access_key | 字符串     |        | 是   | API Key
tonce      | 整型       |        | 是   | 以秒为单位的UNIX timestamp
signature  | 字符串     |        | 是   | 请求签名

### Response

JSON 格式的 [员工对象](#objectemployee) 数组