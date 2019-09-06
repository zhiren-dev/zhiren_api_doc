---
title: 获取员工打卡记录
position: 6.5
type: get

---

**GET** `/v2/employees/:guid/attendance_checkings`
{: .success }

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
start_date | 字符串 |        | 是   | 查询开始日期
end_date | 字符串 |        | 是   | 查询结束日期

### Response

JSON 格式的 [打卡对象](#objectattendance_checking) 数组
