---
title: 获取单个分公司
position: 3.2
type: get
---

**GET** `/api/v2/sub_companies/:sub_company_uuid`
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

JSON 格式的 [分公司对象](#objectsub_company)