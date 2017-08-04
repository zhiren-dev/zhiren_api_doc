# Vacancy - 招聘职位

## Recruitments::Vacancy 对象

### Oauth2 接口

属性      | 类型   | 默认值 | 描述
----------|--------|--------|------|
uuid      | 字符串 |        |
head_count| 字符串 |        | 招聘人数
status    | 枚举串 |        | 状态
department_uuid    | 字符串 |        | 部门id
department_name    | 字符串 |        | 部门名
job_title_uuid     | 字符串 |        | 职位id
job_title_name     | 字符串 |        | 职位名


## Get All Vacancies - 获得公司全部招聘职位的信息

### HTTP Request

`GET /api/v2/recruitments/vacancies`

### HTTP Parameters

参数       | 类型       | 默认值 | 必须 | 描述
-----------|------------|--------|------|----------------------------|
access_token | 字符串     |        | 是   | API Key
### Response

JSON 格式的 VacancyPresenter 对象数组

```json
[
  {
    "uuid": "2387c26da1091124264793e123744fbb",
    "head_count": "3",
    "status: "normal",
    "department_uuid": "3387c26da1091124264793e123744fbb",
    "department_name": "设计部",
    "job_title_uuid": "4387c26da1091124264793e123744fbb",
    "job_title_name": "设计师",
  },
  {
    "uuid": "2487c26da1091124264793e123744fbb",
    "head_count": "1",
    "status: "normal",
    "department_uuid": "3487c26da1091124264793e123744fbb",
    "department_name": "研发部",
    "job_title_uuid": "4487c26da1091124264793e123744fbb",
    "job_title_name": "工程师",
  }

]
```


## Get the Vacancy by uuid - 根据uuid查找某一招聘职位的信息

### HTTP Request

`GET /api/v2/recruitments/vacancy/:id`

### HTTP Parameters

参数       | 类型       | 默认值 | 必须 | 描述
-----------|------------|--------|------|----------------------------|
access_token | 字符串     |        | 是   | API Key

### Response

JSON 格式的 Vacancy 对象

```json

{
  "uuid": "2387c26da1091124264793e123744fbb",
  "head_count": "3",
  "status: "normal",
  "department_uuid": "3387c26da1091124264793e123744fbb",
  "department_name": "设计部",
  "job_title_uuid": "4387c26da1091124264793e123744fbb",
  "job_title_name": "设计师",
}

```
