---
title: 导入员工打卡记录
position: 6.2
type: post
---

**POST** `/api/v2/attendance_punches`
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
attendances | 哈希数组 |        | 是   | 打卡记录

~~~ ruby
attendances: [
  { "empno": "NORMAL-1", "punched_at": "2017-02-03 08:00" },
  { "empno": "1100", "punched_at": "2017-02-03 08:00" },
  { "empno": "1100", "punched_at": "2017-02-03 08:00" }
]
~~~

### Response

包含传递过来的每一条打卡数据的状态，格式为：
~~~ ruby
[{ code: "0k", empno: "007" }, { code: "error", empno: "008", error_message: "employee not found" }]
~~~