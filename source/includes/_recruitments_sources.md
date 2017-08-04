# Source -招聘源

## Recruitments::Source 对象

### Oauth2 接口

属性      | 类型   | 默认值 | 描述
----------|--------|--------|------|
uuid      | 字符串 |        |
name      | 字符串 |        | 来源名

## Get All Sources - 获得公司全部招聘源信息

### HTTP Request

`GET /api/v2/recruitments/sources`

### HTTP Parameters

参数       | 类型       | 默认值 | 必须 | 描述
-----------|------------|--------|------|----------------------------|
access_token | 字符串     |        | 是   | API Key
### Response

JSON 格式的 SourcePresenter 对象数组

```json
[
  {
    "uuid": "2387c26da1091124264793e123744fbb",
    "name": "拉勾",
  },
  {
    "uuid": "2587c26da1091124264793e123744fbb",
    "name": "51job",
  }

]
```


## Get the Source by uuid - 根据uuid查找某一招聘源的信息

### HTTP Request

`GET /api/v2/recruitments/source/:id`

### HTTP Parameters

参数       | 类型       | 默认值 | 必须 | 描述
-----------|------------|--------|------|----------------------------|
access_token | 字符串     |        | 是   | API Key

### Response

JSON 格式的 Source 对象

```json

{
  "uuid": "2587c26da1091124264793e123744fbb",
  "name": "拉勾",
}
```
