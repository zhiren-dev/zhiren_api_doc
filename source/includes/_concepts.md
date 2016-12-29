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

属性      | 类型    | 默认值 | 必须 | 描述
----------|---------|--------|------|------------------------------------------------|
name      | string  |        | yes  | 姓名
sex       | integer |        | yes  | 性别（0 表示男性，1 表示女性）
email     | string  |        | yes  | 邮箱
mobile    | string  |        | yes  | 手机号
id_number | string  |        | yes  | 身份证号码
address   | string  |        | yes  | 住址
bank_card | string  |        | yes  | 银行卡号
phone     | string  |        | yes  | 照片
marriage  | integer |        | yes  | 婚姻状况（0 表示单身，1 表示已婚，2 表示离异）
birthday  | string  |        | yes  | 生日
join_date | string  |        | yes  | 入职日期

