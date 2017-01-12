# NotifyEmployees - 员工提醒

## Employee 对象

属性      | 类型   | 默认值 | 描述
----------|--------|--------|------|
uuid      | 字符串 |        |
name      | 字符串 |        | 姓名
sex       | 枚举串 |        | 性别
email     | 字符串 |        | 邮箱
mobile    | 字符串 |        | 手机号
phone_number | 字符串|      | 手机号
id_number | 字符串 |        | 身份证号
address   | 字符串 |        | 详细地址
bank_card | 字符串 |        | 银行卡号
photo     | 字符串 |        | 头像
marriage  | 字符串 |        | 婚姻状况
birthday  | 字符串 |        | 公历生日
join_date | 日期   |        | 入职日期
avatar    | 字符串 |        | 头像

## Notify Employee By Guid - 提醒员工接见访客

### HTTP Request

`POST /api/v2/employees/:guid/notify`

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

Employee 对象
