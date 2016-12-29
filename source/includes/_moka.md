# Moka - 招聘 CRM

## Create candidates - 创建候选人

### HTTP Request

`POST /api/v2/moka_candidates`

### HTTP Parameters

参数       | 类型       | 默认值 | 必须 | 描述
-----------|------------|--------|------|----------------------------|
payload    | JSON字符串 |        | 是   | JSON Payload
access_key | 字符串     |        | 是   | API Key
tonce      | 整型       |        | 是   | 以秒为单位的UNIX timestamp
signature  | 字符串     |        | 是   | 请求签名

### Payload Schema

```
{
  "id": "6XYfZGL4RWFfjSEpsEpdJ2eB",
  "name": "张三",
  "phone": "13203030303",
  "email": "a@b.com",
  "gender": "男",
  "birthYear": 1990,
  "source": "拉勾网",
  "academicDegree": "本科",
  "married": "未婚",
  "educationInfo": [
    {
      "startDate": "2007-09",
      "endDate": "2011-09",
      "school": "北京大学",
      "speciality": "数学与应用数学",
      "academicDegree": "理学学士"
    }
  ],
  "experienceInfo": [
    {
      "startDate": "2012-05",
      "endDate": "2014-05",
      "company": "腾讯广研",
      "title": "前端工程师"
    }
  ],
  "resumeUrl": "http://url.com/file",
  "jobTitle": "前端工程师",
  "operator": {
    "name": "李四",
    "email": "lisi@a.com",
    "phone": "15828748567"
  },
  "interviewFeedbackUrl": "http://url.com/file",
  "offerAttachmentUrls": "",
  "offerInfo": ""
}
```

属性  | 类型   | 默认值 | 必须 | 描述
------|--------|--------|------|-------------------|
id                   | string |    | 是 | 候选人在 Moka 中的 id
name                 | string |    | 是 | 姓名
phone                | string |    | 是 | 电话
email                | string |    | 是 | 邮箱
jobTitle             | string |    | 是 | 申请的职位名称
operator             | hash   |    | 是 | Moka 操作人
gender               | string |    | 否 | 性别, 男、女
birthYear            | integer|    | 否 | 出生年份，1990
source               | string |    | 否 | 渠道， 拉勾
academicDegree       | string |    | 否 | 学历，['本科', '硕士', '博士', '高中', '大专', '中专''MBA', '其他']
married              | string |    | 否 | ['已婚', '未婚', '离异']
educationInfo        | hash   |    | 否 | 教育经历
experienceInfo       | hash   |    | 否 | 工作经历
resumeUrl            | string |    | 否 | 简历下载url
interviewFeedbackUrl | string |    | 否 | 面试反馈文件下载url
offerAttachmentUrls  |        |    | 否 | offer 附件下载
offerInfo            | hash   |    | 否 | offer 信息

### Response

`{ error_code: 0, error_message: 'ok' }`
