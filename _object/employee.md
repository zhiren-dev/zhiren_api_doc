---
title: 员工
position: 4
---

Employee
{: .success }

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
status     | 字符串 |       | 员工状态，详见说明
department_uuid | 字符串 |       | 所在部门唯一标示符
exmail | 字符串 |       | 企业邮箱地址
job_title |字符串| |职位|
job_grade |字符串| |职级|
nickname |字符串| |昵称|
dingtalk_id |字符串| |钉钉 ID|
leader_uuid |字符串| |汇报人唯一标识符|
virtual_leader_uuid |字符串| |虚线汇报人唯一标识符|

### 员工状态说明
waiting
: 待入职

regular
: 在职

dimission
: 离职