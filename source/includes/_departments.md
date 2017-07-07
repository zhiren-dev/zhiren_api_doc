# Departments - 部门

## Department 对象

属性      | 类型   | 默认值 | 描述
----------|--------|--------|------|
name      | 字符串 |         | 部门名称
uuid       | 字符串 |        | 部门唯一标识符
superior_uuid | 字符串 |     | 上级部门唯一标识符
charger_uuid | 字符串 |     | 部门负责人唯一标识符


## Get All Departments - 获得公司全部部门的信息

### HTTP Request

`GET /api/v2/departments`

### HTTP Parameters

参数       | 类型       | 默认值 | 必须 | 描述
-----------|------------|--------|------|----------------------------|
access_key | 字符串     |        | 是   | API Key
tonce      | 整型       |        | 是   | 以秒为单位的UNIX timestamp
signature  | 字符串     |        | 是   | 请求签名

### Response

JSON 格式的 Department 对象数组

```json
[
    {
        "name": "管理组",
        "uuid": "7684be70c34c554c8fdc062eba4382be",
        "superior_uuid": null,
        "charger_uuid": "fbfd8384fb43da1d979fd277473d7984"
    },
    {
        "name": "运营组",
        "uuid": "8674be70c34c554c8fdc062eba4382be",
        "superior_uuid": null,
        "charger_uuid": "fbfd8384fb43da1d979fd277473d7984"
    },
    {
        "name": "系统组",
        "uuid": "8689be70c34c554c8fdc062eba4382be",
        "superior_uuid": null,
        "charger_uuid": "fbfd8384fb43da1d979fd277473d7984"
    },
    {
        "name": "知人",
        "uuid": "8684qe70c34c554c8fdc062eba4382be",
        "superior_uuid": null,
        "charger_uuid": "fbfd8384fb43da1d979fd277473d7984"
    },
    {
        "name": "Tower",
        "uuid": "8684be00c34c554c8fdc062eba4382be",
        "superior_uuid": null,
        "charger_uuid": "fbfd8384fb43da1d979fd277473d7984"
    },
    {
        "name": "行政组",
        "uuid": "8684be70c34c524c8fdc062eba4382be",
        "superior_uuid": null,
        "charger_uuid": "fbfd8384fb43da1d979fd277473d7984"
    },
    {
        "name": "产品组",
        "uuid": "8684be70c34c554c8fdc062eba4382ke",
        "superior_uuid": null,
        "charger_uuid": "fbfd8384fb43da1d979fd277473d7984"
    },
    {
        "name": "移动客户端",
        "uuid": "8684be70c34c554c8fdc062eba4382bp",
        "superior_uuid": null,
        "charger_uuid": "fbfd8384fb43da1d979fd277473d7984"
    },
    {
        "name": "测试部门",
        "uuid": "49c932694bcab42f688863561cf746e1",
        "superior_uuid": "8684be70c34c554c8fdc062eba4382be",
        "charger_uuid": "fbfd8384fb43da1d979fd277473d7984"
    }
]
```

## Get the Department by uuid - 根据部门唯一标识符查找某一部门的信息

### HTTP Request

`GET /api/v2/departments/:uuid`

### HTTP Parameters

参数       | 类型       | 默认值 | 必须 | 描述
-----------|------------|--------|------|----------------------------|
access_key | 字符串     |        | 是   | API Key
tonce      | 整型       |        | 是   | 以秒为单位的UNIX timestamp
signature  | 字符串     |        | 是   | 请求签名

### Response

JSON 格式的 Department 对象

```json
{
    "name": "管理组",
    "uuid": "7684be70c34c554c8fdc062eba4382be",
    "superior_uuid": null,
    "charger_uuid": "fbfd8384fb43da1d979fd277473d7984"
}
```

## Get the Employees under the Department by uuid - 根据部门唯一标识符查找某一部门下全部员工的信息
### HTTP Request

`GET /api/v2/departments/:uuid/employees`

### HTTP Parameters

参数       | 类型       | 默认值 | 必须 | 描述
-----------|------------|--------|------|----------------------------|
access_key | 字符串     |        | 是   | API Key
tonce      | 整型       |        | 是   | 以秒为单位的UNIX timestamp
signature  | 字符串     |        | 是   | 请求签名

### Response

JSON 格式的 Employee 对象数组

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
