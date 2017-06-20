# Employees - 员工

## Employee 对象

属性      | 类型   | 默认值 | 描述
----------|--------|--------|------|
uuid      | 字符串 |        |
name      | 字符串 |        | 姓名
sex       | 枚举串 |        | 性别
email     | 字符串 |        | 邮箱
mobile    | 字符串 |        | 手机号
empno     | 字符串 |        | 员工编号
phone_number | 字符串|      | 手机号
id_number | 字符串 |        | 身份证号
address   | 字符串 |        | 详细地址
bank_card | 字符串 |        | 银行卡号
photo     | 字符串 |        | 头像
marriage  | 字符串 |        | 婚姻状况
birthday  | 字符串 |        | 公历生日
join_date | 日期   |        | 入职日期
avatar    | 字符串 |        | 头像
leave_date | 日期  |        | 离职日期
status     | 字符串 |       | 员工状态，"regular" 表示在职，"dimission" 表示离职。
department_uuid | 字符串 |       | 所在部门唯一标示
exmail | 字符串 |       | 企业邮箱地址
job_title |字符串| |职位|



## Get All Employees - 获得公司全部员工的信息

### HTTP Request

`GET /api/v2/employees`

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

JSON 格式的 EmployeePresenter 对象数组


## Get the Employee by Mobile - 根据员工手机号查找某一员工的信息

### HTTP Request

`GET /api/v2/employees/:mobile`

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

JSON 格式的 Employee 对象
