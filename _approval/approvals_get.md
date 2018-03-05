---
title: 获取审批列表
position: 12.1
type: get
right_code: |
  ~~~ json
  [
    {
      "number_series": "20170612296548",
      "creator": "孙秀",
      "created_at": "2017年6月12日 下午19点05分",
      "status": "passed",
      "status_name": "通过",
      "updated_at": "2017年6月12日 下午19点05分",
      "category": "onboarding",
      "workflow_name": "员工入职",
      "form_values": {
        "社保公积金": {
          "参缴方案": "公积金方案_1",
          "社保基数": 800.0,
          "公积金基数": 600.0,
          "生效日期": "2017-06"
        },
        "考勤规则": {
          "考勤规则": "排班规则_1"
        },
        "假期发放规则": {
          "假期_1": "手动发放"
        }
      }
    },
    {
      "number_series": "20170708347419",
      "creator": "张布",
      "created_at": "2017年7月8日 上午08点58分",
      "status": "passed",
      "status_name": "通过",
      "updated_at": "2017年7月8日 上午08点59分",
      "category": "business_travel",
      "workflow_name": "出差申请",
      "form_values": {
        "开始日期": "2017-07-08",
        "开始日期时间段": "全天",
        "结束日期": "2017-07-10",
        "结束日期时间段": "全天",
        "出差时长": 3.0,
        "原因": "出差",
        "申请调休假": 0,
        "有效时间": 180
      }
    }
  ]
  ~~~
  {: title="Response" }
---
---


本接口开发中
{: .error }


**GET** `/api/v2/approvals`
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
  "start_date": "2018-02-01",              # 发起审批开始日期
  "end_date": "2018-03-01"                 # 发起审批截止日期
}
```
{: title="payload 数据结构" }


### Response

JSON 格式的 [审批对象](#objectapproval) 数组