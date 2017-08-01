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
department_uuid | 字符串 |       | 所在部门唯一标示符
exmail | 字符串 |       | 企业邮箱地址
job_title |字符串| |职位|
job_grade |字符串| |职级|
nickname |字符串| |昵称|
dingtalk_id |字符串| |钉钉 ID|
leader_uuid |字符串| |汇报人唯一标识符|
virtual_leader_uuid |字符串| |虚线汇报人唯一标识符|




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
token | 字符串 |        | 是   | 区别公司的标识符
status | 字符串 | all   | 否   | 员工状态, waiting: 待入职, joined: 在职, dimission: 离职

### Response

JSON 格式的 EmployeePresenter 对象数组

```json
[
  {
    "uuid": "1387c26da1091124264793e123744fbb",
    "name": "一般职员",
    "sex": "male",
    "empno": "NORMAL-1",
    "email": "76577261@qq.com",
    "mobile": "18602836721",
    "phone_number": "18602836721",
    "id_number": "320581199406301913",
    "address": "烨伟路313号",
    "bank_card": "",
    "photo": "",
    "marriage": "divorced",
    "birthday": "1983-07-21",
    "join_date": "2012-09-29",
    "avatar": "",
    "leave_date": null,
    "status": "waiting",
    "department_uuid": "f46594b15bc947891fcf8700f3aaa2ba",
    "exmail": "test1@colorway.com",
    "job_title": "CTO",
    "job_grade": "",
    "dingtalk_id": null,
    "nickname": "少林扫地僧",
    "leader_uuid": null,
    "virtual_leader_uuid": "fbfd8324fb43da1d979fd277473d7984"
  },
  {
    "uuid": "fbfd8384fb43da1d979fd277473d7984",
    "name": "一般职员",
    "sex": "male",
    "empno": "NORMAL-1",
    "email": "337261@qq.com",
    "mobile": "18689992211",
    "phone_number": "18689992211",
    "id_number": "230581199406301913",
    "address": "烨伟路313号",
    "bank_card": "",
    "photo": "",
    "marriage": "divorced",
    "birthday": "1989-02-21",
    "join_date": "2012-08-09",
    "avatar": "",
    "leave_date": null,
    "status": "waiting",
    "department_uuid": "f46594b15bc947891fcf8700f3aaa2ba",
    "exmail": "test2@colorway.com",
    "job_title": "CTO",
    "job_grade": "",
    "dingtalk_id": null,
    "nickname": "少林扫地僧",
    "leader_uuid": "fbfd8384fb43da1d979fd277473d7982",
    "virtual_leader_uuid": null
  }

]
```


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

```json

{
  "uuid": "1387c26da1091124264793e123744fbb",
  "name": "一般职员",
  "sex": "male",
  "empno": "NORMAL-1",
  "email": "76577261@qq.com",
  "mobile": "18602836721",
  "phone_number": "18602836721",
  "id_number": "320581199406301913",
  "address": "烨伟路313号",
  "bank_card": "",
  "photo": "",
  "marriage": "divorced",
  "birthday": "1983-07-21",
  "join_date": "2012-09-29",
  "avatar": "",
  "leave_date": null,
  "status": "waiting",
  "department_uuid": "f46594b15bc947891fcf8700f3aaa2ba",
  "exmail": "test1@colorway.com",
  "job_title": "CTO",
  "job_grade": "",
  "dingtalk_id": null,
  "nickname": "少林扫地僧",
  "leader_uuid": null,
  "virtual_leader_uuid": "fbfd8324fb43da1d979fd277473d7984"
}

```
## Get the Employee by uuid - 根据唯一标识符查找某一员工的信息

### HTTP Request

`GET /api/v2/employees/:uuid`

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

```json

{
  "uuid": "1387c26da1091124264793e123744fbb",
  "name": "一般职员",
  "sex": "male",
  "empno": "NORMAL-1",
  "email": "76577261@qq.com",
  "mobile": "18602836721",
  "phone_number": "18602836721",
  "id_number": "320581199406301913",
  "address": "烨伟路313号",
  "bank_card": "",
  "photo": "",
  "marriage": "divorced",
  "birthday": "1983-07-21",
  "join_date": "2012-09-29",
  "avatar": "",
  "leave_date": null,
  "status": "waiting",
  "department_uuid": "f46594b15bc947891fcf8700f3aaa2ba",
  "exmail": "test1@colorway.com",
  "job_title": "CTO",
  "job_grade": "",
  "dingtalk_id": null,
  "nickname": "少林扫地僧",
  "leader_uuid": null,
  "virtual_leader_uuid": "fbfd8324fb43da1d979fd277473d7984"
}

```
