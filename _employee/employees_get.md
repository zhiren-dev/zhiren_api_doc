---
title: 获取所有员工
position: 5.1
type: get

---

**GET** `/api/v2/employees`
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
token | 字符串 |        | 是   | 区别公司的标识符
status | 字符串 | all   | 否   | [员工状态](#objectemployee)
join_date_start | 字符串 |   | 否   | 入职开始日期，格式: '2017-10-01'
join_date_end | 字符串 |   | 否   | 入职截止日期
leave_date_start | 字符串 |   | 否   | 离职开始日期
leave_date_end | 字符串 |   | 否   | 离职截止日期
name | 字符串 |   | 否   | 员工姓名
pagination | JSON字符串 |   | 否 | 分页获取员工数据，详见 pagination schema

**Pagination Schema**

属性  | 类型   | 默认值 | 必须 | 描述
------|--------|--------|------|-------------------|
page | 整型 |        | 是 | 获取第几页员工数据

### Response

**全部获取时**

JSON 格式的 [员工对象](#objectemployee) 数组

**分页获取时**

属性  | 类型   | 描述
-----|--------|-------|
currentPage | 整型 | 当前页码
pageSize | 整型 | 每页数量
totalPages | 整型 | 总页数
totalCount | 整型 | 总数据量
employees | 数组 | JSON 格式的 [员工对象](#objectemployee) 数组

