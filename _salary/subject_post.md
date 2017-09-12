---
title: 薪酬科目上传
position: 10.2
type: post
---

本接口开发中
{: .error }

**POST** `/api/v2/salary/subjects`
{: .success }


### HTTP Parameters

参数       | 类型       | 默认值 | 必须 | 描述
-----------|------------|--------|------|----------------------------|
payload    | JSON字符串 |        | 是   | JSON Payload
access_key | 字符串     |        | 是   | API Key
tonce      | 整型       |        | 是   | 以秒为单位的UNIX timestamp
signature  | 字符串     |        | 是   | 请求签名


``` ruby
{
  "empno": "001",              # 员工工号
  "subject_name": "绩效工资",   # 薪酬科目名称
  "month": "2017-09",          # 计薪月份，格式: "yyyy-mm"
  "value": 1024.12             # 金额，精确到小数点后两位
}
```
{: title="payload 数据结构" }

同一员工薪酬如果上传多次（相同月份），则以最后一次数据为准
{: .warning }

### Response

~~~ ruby
  { "code": "返回码", "text": "error message" } # 0 表示成功
~~~
