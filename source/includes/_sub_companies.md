# SubCompany - 子公司

## SubCompany 对象

属性      | 类型   | 默认值 | 描述
----------|--------|--------|------|
uuid      | 字符串 |        | 分公司唯一标识符
company_uuid      | 字符串 |        | 母公司唯一标识符
name       | 字符串 |        | 分公司名称
short_name       | 字符串 |        | 分公司简称
registered_address  | 字符串 |        | 注册地址
boss  | 字符串 |        | 法人姓名


## Get All SubCompanies - 获得所有分公司的信息

### HTTP Request

`GET /api/v2/sub_companies`

### HTTP Parameters

参数       | 类型       | 默认值 | 必须 | 描述
-----------|------------|--------|------|----------------------------|
access_key | 字符串     |        | 是   | API Key
tonce      | 整型       |        | 是   | 以秒为单位的UNIX timestamp
signature  | 字符串     |        | 是   | 请求签名

### Response

JSON 格式的 SubCompany 对象数组


## Get The SubCompany By SubCompanyUUID - 根据分公司 SubCompanyUUID 获取某个分公司的信息

### HTTP Request

`GET /api/v2/sub_companies/:sub_company_uuid`

### HTTP Parameters

参数       | 类型       | 默认值 | 必须 | 描述
-----------|------------|--------|------|----------------------------|
access_key | 字符串     |        | 是   | API Key
tonce      | 整型       |        | 是   | 以秒为单位的UNIX timestamp
signature  | 字符串     |        | 是   | 请求签名

### Response

JSON 格式的 SubCompany 对象


## Get All Employees Under The SubCompany By SubCompanyUUID - 根据分公司的 SubCompanyUUID 获取某个分公司所有员工的信息

### HTTP Request

`GET /api/v2/sub_companies/:sub_company_uuid/employees`

### HTTP Parameters

参数       | 类型       | 默认值 | 必须 | 描述
-----------|------------|--------|------|----------------------------|
access_key | 字符串     |        | 是   | API Key
tonce      | 整型       |        | 是   | 以秒为单位的UNIX timestamp
signature  | 字符串     |        | 是   | 请求签名

### Response

JSON 格式的 Employee 对象数组

## Get One Employee Under The SubCompany By SubCompanyUUID - 根据分公司的 SubCompanyUUID 获取某个分公司某个员工的信息

### HTTP Request

`GET /api/v2/sub_companies/:sub_company_uuid/employees/:uuid`

### HTTP Parameters

参数       | 类型       | 默认值 | 必须 | 描述
-----------|------------|--------|------|----------------------------|
access_key | 字符串     |        | 是   | API Key
tonce      | 整型       |        | 是   | 以秒为单位的UNIX timestamp
signature  | 字符串     |        | 是   | 请求签名

### Response

JSON 格式的 Employee 对象数组
