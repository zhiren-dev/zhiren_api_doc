---
title: 更新日志
position: 4
---
`2016-09-09` <br/>创建文档
{: .info }

`2016-12-29` <br/>新增员工提醒、出勤员工、Moka 候选人 API
{: .info }

`2017-01-08` <br/>新增获取子公司、子公司部门、子公司员工信息的 API
{: .info }

`2017-01-17` <br/>新增绑定、解绑 Moka 公司以及查询 bind_code 有效性的 API
{: .info }

`2017-03-18` <br/>新增出勤打卡 API
{: .info }

`2017-06-06` <br/>Department 对象去掉 sub_company 字段，移除如下接口：
<br/>`GET /api/v2/sub_companies/:sub_company_uuid/departments`
<br/>`GET /api/v2/sub_companies/:sub_company_uuid/departments/:uuid`
{: .info }

`2017-06-20` <br/>`Employee` 对象中新增 `job_title` 字段
{: .info }

`2017-07-07` <br/>`Employee` 对象中新增 `leader_uuid`, `virtual_leader_uuid` 字段，`Department` 对象中新增 `charger_uuid` 字段，新增根据 uuid 查找员工信息
{: .info }