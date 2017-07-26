# Timelines - 请假或者公出信息

## Timelines 对象

 属性            | 类型  | 默认值 | 描述         |
----------------|---------|--------|----------------------|
 date           | 日期    |        | 发生日期             |
 category       | 字符串  |        | leave/business_trip |
 duration       | 数字    |        | 时间         |
 duration_unit  | 字符串 |        |  days/hours/minutes |
 start_time     | 时间    |        | 开始时间      |
 end_time       | 时间    |        | 结束时间      |

## Timelines - 检查某位员工某段时间的请假或者公出信息

### HTTP Request

`get /api/v2/employees/:guid/timelines`


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
category   | 字符串     |        | 是   | leave/business_trip

### Response

Timeline 对象的数组
