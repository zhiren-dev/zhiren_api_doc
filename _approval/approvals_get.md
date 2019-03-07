---
title: 获取审批列表
position: 12.1
type: get
right_code: |
  ~~~ json
  [
    {
      "number_series": "20170712355448",
      "creator": "辛宪英",
      "created_at": "2017-07-12T17:29:30.000+08:00",
      "status": "denied",
      "status_name": "不通过",
      "updated_at": "2017-07-12T17:30:51.000+08:00",
      "category": "dimission",
      "workflow_name": "员工离职",
      "form_values": [
        {
          "section": "行政审批",
          "fields": [
            {
              "name": "确认办公用品是否归还",
              "value": "否"
            }
          ]
        },
        {
          "section": "财务结算",
          "fields": [
            {
              "name": "停薪日期",
              "value": "2017-07-12"
            }
          ]
        },
        {
          "section": "款项结算",
          "fields": [
            {
              "name": "确认是否还有未结往来款项",
              "value": "否"
            }
          ]
        },
        {
          "section": "服务关闭",
          "fields": [
            {
              "name": "公司邮箱",
              "value": "否"
            }
          ]
        }
      ]
    },
    {
      "number_series": "20170721372181",
      "creator": "袁绍",
      "created_at": "2017-07-21T16:00:06.000+08:00",
      "status": "passed",
      "status_name": "通过",
      "updated_at": "2017-07-21T16:00:09.000+08:00",
      "category": "onboarding",
      "workflow_name": "员工入职",
      "form_values": [
        {
          "section": "适用规则",
          "fields": [
            {
              "name": "假期发放规则",
              "value": {
                "假期_11": null,
                "假期_1": null
              }
            }
          ]
        }
      ]
    }
  ]
  ~~~
  {: title="Response" }
---
---


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
  "end_date": "2018-03-01",                # 发起审批截止日期
  "category": "leave"                      # 审批类型，不传该参数代表获取所有审批类型
}
```
{: title="payload 数据结构" }

### 审批类型参数列表

参数                   | 类型
----------------------|------------|
leave                 | 请假
adjustment            | 员工调整
contract              | 合同签署
dimission             | 员工离职
enrollment            | 员工转正
payroll_submit        | 工资表审批
recruit               | 重新入职
salary_change         | 薪资调整
attendance_recheck    | 补签
overtime              | 加班
business_trip         | 公出
sub_company_transfer  | 分公司调动
onboarding            | 员工入职
business_travel       | 出差
intern_regularization | 实习生转全职
breastfeeding_leave   | 哺乳假申请
duty                  | 值班申请
arrangement           | 调班申请
custom                | 自定义审批


### Response

JSON 格式的 [审批对象](#objectapproval) 数组
