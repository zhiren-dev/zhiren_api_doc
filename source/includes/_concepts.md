# Concepts - 概念

### Company - 公司

每当一家公司在知人开通服务，系统就会创建一条 Company 记录。

#### Company 对象属性

属性      | 类型   | 默认值 | 必须 | 描述
----------|--------|--------|------|------------------------------|
uuid      | string |        | yes  | 用于唯一区分一家公司的标识符
name      | string |        | yes  | 公司名称
full_name | string |        | no   | 公司全称
logo      | string |        | no   | 公司 logo URL

### Employee - 员工

一个公司拥有多个员工。员工是本系统核心概念之一。

#### Employee 对象属性

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
department_uuid | 字符串 |       | 所在部门唯一标示符
exmail | 字符串 |       | 企业邮箱地址
job_title |字符串| |职位|
job_grade |字符串| |职级|
nickname |字符串| |昵称|
dingtalk_id |字符串| |钉钉 ID|
leader_uuid |字符串| |汇报人唯一标识符|
virtual_leader_uuid |字符串| |虚线汇报人唯一标识符|
