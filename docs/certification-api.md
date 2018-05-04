# 机构认证 API 文档

## 获取机构认证信息

`api/v2/tbm/certification`

## 请求方法

`get `

## 请求体

无

### HTTP Status Code

200

## 返回体

```json5
{
    "id": 1,
    "certification_name": "project_party",
    "user_id": 2,
    "data": {
        "name": "vicnent",
        "phone": "13547899124",
        "number": "123456",
        "number_type": "passport",
        "images": "12,13",
        "letter": "1"
    },
    "examiner": 0,
    "status": 1,
    "created_at": "2018-03-01 02:04:41",
    "updated_at": "2018-03-01 02:25:12",
    "icon": null,
    "category": {
        "name": "project_party",
        "display_name": "区块链项目方",
        "description": null
    },
    "user": {
        "id": 2,
        "name": "vincent",
        "bio": null,
        "sex": 0,
        "location": null,
        "created_at": "2018-02-28 10:00:29",
        "updated_at": "2018-02-28 10:00:29",
        "avatar": null,
        "bg": null,
        "verified": {
            "type": "project_party",
            "icon": null
        },
        "extra": null
    }
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|name|string		|yes		   |主体名称  |
|phone|string		|yes		   |认证电话号码  |
|number|string		|yes		   |证件号码  |
|number_type|string		|yes		   |认证类型  |
|images|array		|yes		   |认证图片ID  |
|letter|array		|yes		   |公函ID  |

## 认证

`api/v2/tbm/certification`

## 请求方法

`post `

## 请求体

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| type    | string      | yes       |  认证类型 企业：enterprise 项目方：project_party 媒体：media 社团组织：organization  |
| name    | string      | yes       |  主体名称  |
| phone    | string      | yes       |  电话号码  |
| number    | string      | yes       |  证件号码  |
| number_type    | string      | yes       |  证件类型 id_card：身份证 passport：护照  |
| images    | string      | yes       |  证件图片ID : example:"images": 1, 2 |
| letter    | string      | yes       |  公函图片ID  |
| business_name    | string      | yes       |  姓名  |
| business_num    | string      | yes       |  营业执照号码  |
| business_license    | int      | yes       |  营业执照图片ID  |

### HTTP Status Code

201

## 返回体

```json5
{
    "message": [
           "申请成功，等待审核"
       ]
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|message|string		|yes		   |错误信息描述  |


## 更新机构认证

`api/v2/tbm/certification`

## 请求方法

`patch `

## 请求体

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| type    | string      | yes       |  认证类型 企业：enterprise 项目方：project_party 媒体：media 社团组织：organization  |
| phone    | string      | yes       |  电话号码  |
| number    | string      | yes       |  证件号码  |
| number_type    | string      | yes       |  证件类型 id_card：身份证 passport：护照|
| images    | string      | yes       |  证件图片ID : example:"images": 1, 2 |
| letter    | string      | yes       |  公函图片ID  |
| business_name    | string      | yes       |  姓名  |
| business_num    | string      | yes       |  营业执照号码  |
| business_license    | int      | yes       |  营业执照图片ID  |
### HTTP Status Code

201

## 返回体

```json5
{
    "message": [
           "修改成功，等待审核"
       ]
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|message|string		|yes		   |错误信息描述  |