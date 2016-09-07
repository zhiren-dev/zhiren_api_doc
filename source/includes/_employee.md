# Employees - 员工

## Get All Employees

### HTTP Request

`GET /api/v1/employees`

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
token | 字符串 |        | 是   | 区别公司 的标识符

### Response

Employee 对象数组

属性      | 类型   | 默认值 | 描述
----------|--------|--------|------|
name      | 字符串 |        | 姓名
sex       | 字符串 |        |
email     | 字符   |        |
mobile    | 字符   |        |
id_number | 字符   |        |
address   | 字符   |        |
bank_card | 字符   |        |
photo     | 字符   |        |
marriage  | 字符   |        |
birthday  | 字符   |        |
join_date | 字符   |        |
