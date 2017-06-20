# Changelog - 变更历史

## API changelog

暂无。

## API documentation Changelog

* 2016-09-09 补充 API host（https://zhiren.com/api/v1/<apiname>）
* 2016-12-29 新增员工提醒、出勤员工、Moka 候选人 API
* 2017-01-08 新增获取子公司、子公司部门、子公司员工信息的 API
* 2017-01-17 新增绑定、解绑 Moka 公司以及查询 bind_code 有效性的 API
* 2017-03-18 新增出勤打卡 API
* 2017-06-06 Department 对象去掉 sub_company 字段，移除 `GET /api/v2/sub_companies/:sub_company_uuid/departments` 和 `GET /api/v2/sub_companies/:sub_company_uuid/departments/:uuid` 接口
* 2017-06-20 Employee 对象中新增 job_title 字段
