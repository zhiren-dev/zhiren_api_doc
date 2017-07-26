# Attendance Checking - 打卡信息

## Attendance Checking 对象

 属性           | 类型  | 默认值 | 描述         |
----------------|-------|--------|--------------|
 date           |  日期 |        | 打卡日期     |
 check_in_time  | 时间  |        | 上班打卡时间 |
 check_out_time | 时间  |        | 下班打卡时间 |

## Attendance checkings - 检查某位员工某段时间的打卡记录

### HTTP Request

`GET /api/v2/employees/:guid/attendance_checkings`

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

### Respoonse

Attendance Checking 对象的数组
