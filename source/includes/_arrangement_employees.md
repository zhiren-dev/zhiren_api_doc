# Arrangement Employees - 员工排班

## 排班对象

属性      | 类型   | 默认值 | 描述
----------|--------|--------|------|
attenance_rule_name      | 字符串 |        | 出勤规则名称
workshift_name      | 字符串 |        | 班次
empno       | 枚举串 |        | 员工工号
date     | 字符串 |        | 排班日期
time_range    | 字符串 |        | 工作时间段


### HTTP Request

`GET /api/v2/arrangement_employees`

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

排班对象列表
