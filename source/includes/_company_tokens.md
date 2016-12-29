# CompanyTokens - 公司令牌

## CompanyPresenter 对象

属性      | 类型   | 默认值 | 描述
----------|--------|--------|------|
uuid      | 字符串 |        | 姓名
name      | 字符串 |        | 公司简称
full_name | 字符串 |        | 公司全称
logo      | 字符串 |        | logo

## Update The Token - 更新公司令牌

### HTTP Request

`PATCH /api/v2/company_tokens/:guid`

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
zhiren_visitor_token | 字符串 |        | 是   | fangke 提供给 zhiren 的令牌

### Response

CompanyPresenter 对象
