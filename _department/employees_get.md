---
title: 查询部门员工
position: 4.3
type: get
right_code: |
  ~~~ json
  [{
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
  }]
  ~~~
  {: title="Response" }
---
---

**GET** `/api/v2/departments/:uuid/employees`
{: .success }

### HTTP Parameters

参数       | 类型       | 默认值 | 必须 | 描述
-----------|------------|--------|------|----------------------------|
access_key | 字符串     |        | 是   | API Key
tonce      | 整型       |        | 是   | 以秒为单位的UNIX timestamp
signature  | 字符串     |        | 是   | 请求签名

### Response

JSON 格式的 [员工对象](#objectemployee) 数组