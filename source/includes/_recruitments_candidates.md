# Candidate - 候选人

## Recruitments::Candidate 对象

### Oauth2 接口

属性      | 类型   | 默认值 | 描述
----------|--------|--------|------|
uuid      | 字符串 |        |
name      | 字符串 |        | 姓名
email     | 字符串 |        | 电子邮箱
mobile    | 字符串 |        | 手机号
sex       | 枚举串 |        | 性别
marriage    | 枚举串 |        | 婚姻状况
birthday    | 字符串 |        | 生日
degree      | 字符串 |        | 学历
status      | 枚举串 |        | 候选人状态
source_name | 字符串 |        | 招聘源
source_id   | 字符串 |        | 招聘源 id


## Get All Candidates - 获得公司全部候选人的信息

### HTTP Request

`GET /api/v2/recruitments/candidates`

### HTTP Parameters

参数       | 类型       | 默认值 | 必须 | 描述
-----------|------------|--------|------|----------------------------|
access_token | 字符串     |        | 是   | API Key
### Response

JSON 格式的 CandidatePresenter 对象数组

```json
[
  {
    "uuid": "2387c26da1091124264793e123744fbb",
    "name": "关羽",
    "email: "guanyu@gmail.com",
    "mobile": "13412345678",
    "sex": "male",
    "marriage": "singled",
    "birthday": "1990-05-05",
    "degree": "本科",
    "status": "recommended",
    "source_name": "拉勾",
    "source_id": "2487c26da1091124264793e123744fbb"
  },
  {
    "uuid": "2587c26da1091124264793e123744fbb",
    "name": "貂蝉",
    "email: "diaochan@gmail.com",
    "mobile": "13512345678",
    "sex": "female",
    "marriage": "marriaged",
    "birthday": "1992-05-05",
    "degree": "硕士",
    "status": "interviewed",
    "source_name": "51job",
    "source_id": "2687c26da1091124264793e123744fbb"
  }

]
```


## Get the Candidate by uuid - 根据uuid查找某一候选人的信息

### HTTP Request

`GET /api/v2/recruitments/candidate/:id`

### HTTP Parameters

参数       | 类型       | 默认值 | 必须 | 描述
-----------|------------|--------|------|----------------------------|
access_token | 字符串     |        | 是   | API Key

### Response

JSON 格式的 Candidate 对象

```json

{
  "uuid": "2587c26da1091124264793e123744fbb",
  "name": "貂蝉",
  "email: "diaochan@gmail.com",
  "mobile": "13512345678",
  "sex": "female",
  "marriage": "marriaged",
  "birthday": "1992-05-05",
  "degree": "硕士",
  "status": "interviewed",
  "source_name": "51job",
  "source_id": "2687c26da1091124264793e123744fbb"
}
```
