# Departments - 部门

## Department 对象

属性      | 类型   | 默认值 | 描述
----------|--------|--------|------|
name       | 字符串 |        | 部门名称
guid       | 字符串 |        | 部门唯一标识符


## DepartmentPresenter 对象

属性      | 类型   | 默认值 | 描述
----------|--------|--------|------|
name      | 字符串 |         | 部门名称
uuid       | 字符串 |        | 部门唯一标识符
superior_uuid | 字符串 |     | 上级部门唯一标识符
sub_company   | 字符串 |     | 子公司名称


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

JSON 格式的 Departments 对象数组

```
[
    {
        "name": "管理组",
        "uuid": "7684be70c34c554c8fdc062eba4382be",
        "superior_uuid": null,
        "sub_company": "成都彩程软件设计有限公司"
    },
    {
        "name": "运营组",
        "uuid": "8674be70c34c554c8fdc062eba4382be",
        "superior_uuid": null,
        "sub_company": "成都彩程软件设计有限公司"
    },
    {
        "name": "系统组",
        "uuid": "8689be70c34c554c8fdc062eba4382be",
        "superior_uuid": null,
        "sub_company": "成都彩程软件设计有限公司"
    },
    {
        "name": "知人",
        "uuid": "8684qe70c34c554c8fdc062eba4382be",
        "superior_uuid": null,
        "sub_company": "成都彩程软件设计有限公司"
    },
    {
        "name": "Tower",
        "uuid": "8684be00c34c554c8fdc062eba4382be",
        "superior_uuid": null,
        "sub_company": "成都彩程软件设计有限公司"
    },
    {
        "name": "行政组",
        "uuid": "8684be70c34c524c8fdc062eba4382be",
        "superior_uuid": null,
        "sub_company": "成都彩程软件设计有限公司"
    },
    {
        "name": "产品组",
        "uuid": "8684be70c34c554c8fdc062eba4382ke",
        "superior_uuid": null,
        "sub_company": "成都彩程软件设计有限公司"
    },
    {
        "name": "移动客户端",
        "uuid": "8684be70c34c554c8fdc062eba4382bp",
        "superior_uuid": null,
        "sub_company": "成都彩程软件设计有限公司"
    },
    {
        "name": "测试部门",
        "uuid": "49c932694bcab42f688863561cf746e1",
        "superior_uuid": "8684be70c34c554c8fdc062eba4382be",
        "sub_company": "成都彩程软件设计有限公司"
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

JSON 格式的 EmployeePresenter 对象

```
{
    "name": "管理组",
    "uuid": "7684be70c34c554c8fdc062eba4382be",
    "superior_uuid": null,
    "sub_company": "成都彩程软件设计有限公司"
}
```
