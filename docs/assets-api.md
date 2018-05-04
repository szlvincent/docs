# 机构资产 API 文档

## 获取机构信息

`api/v2/tbm/org/assets`

## 请求方法

`get `

## 请求体

无

### HTTP Status Code

200

## 返回体

```json5
{
    "id": 3,
    "name": "hello",
    "email": null,
    "bio": null,
    "sex": 0,
    "location": null,
    "created_at": "2018-03-21 02:22:17",
    "updated_at": "2018-03-27 08:37:47",
    "rank_status": 1,
    "is_band": 0,
    "single": 300,
    "daily": 500,
    "avatar": null,
    "bg": null,
    "verified": null,
    "extra": {
        "user_id": 3,
        "likes_count": 0,
        "comments_count": 1,
        "followers_count": 0,
        "followings_count": 0,
        "updated_at": "2018-04-04 02:52:09",
        "feeds_count": 0,
        "questions_count": 0,
        "answers_count": 0,
        "checkin_count": 3,
        "last_checkin_count": 1
    },
    "new_wallet": {
        "owner_id": 3,
        "balance": 2,
        "total_income": 2,
        "total_expenses": 0,
        "created_at": null,
        "updated_at": "2018-03-24 11:04:55"
    }
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| id    | int      | yes       |  用户ID  |
| name    | string      | yes       |  昵称  |
| email    | string      | yes       |  邮箱  |
| is_band    | int      | yes       |  是否已经绑定账号 1：绑定 0：未绑定  |
| single    | int      | yes       |  单笔转账限制额度  |
| daily    | int      | yes       |  单日转账限制额度  |
| new_wallet    | array      | yes       |  钱包信息  |
| balance    | int      | yes       |  余额  |

## 绑定个人账号

`api/v2/tbm/org/band`

## 请求方法

`post `

## 请求体

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| band_id    | int      | yes       |  绑定的用户ID  |
| band_name    | string      | yes       |  绑定的用户昵称  |
| band_phone    | string      | yes       |  绑定的用户电话  |

### HTTP Status Code

201

## 返回体

```json5
 {
     "id": 1,
     "user_id": 3,
     "band_id": 2,
     "band_name": "客户看看",
     "band_phone": "13547899124",
     "created_at": "2018-04-07 07:38:48",
     "updated_at": "2018-04-07 07:38:48"
 }
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|id|int		|yes		   |记录ID  |
|user_id|int		|yes		   |用户ID  |
|band_id|int		|yes		   |绑定用户ID  |
|band_name|string		|yes		   |绑定用户昵称  |
|band_phone|string		|yes		   |绑定用户电话  |

## 解除绑定

`api/v2/tbm/org/unband`

## 请求方法

`delete `

## 请求体

wu

### HTTP Status Code

204

## 返回体

无

## 返回字段

无

## 转账

`api/v2/tbm/org/transfer`

## 请求方法

`post `

## 请求体

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| mark    | int      | yes       |  转账mark值|
| verifyCode    | string      | yes       |  验证码  |
| trans_id    | int      | yes       |  接收人ID  |
| phone    | string      | yes       |  接收人电话号码  |


### HTTP Status Code

201

## 返回体

```json5
 {
     "message": "转账TBMark值不能超过当日最大设置"
 }
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|message|string		|yes		   |返回信息  |


## 获取手机号码用户信息

`api/v2/tbm/org/phone`

## 请求方法

`get `

## 请求体

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| phone    | string      | yes       |  手机号码|


### HTTP Status Code

200

## 返回体

```json5
 {
     "id": 2,
     "name": "客户看看",
     "email": "123@123.com",
     "bio": null,
     "sex": 0,
     "location": null,
     "created_at": "2018-03-20 07:22:00",
     "updated_at": "2018-04-07 07:10:18",
     "rank_status": 1,
     "avatar": "http://www.tbm.com/api/v2/users/2/avatar",
     "bg": null,
     "verified": {
         "type": "enterprise",
         "icon": null
     },
     "extra": {
         "user_id": 2,
         "likes_count": 1,
         "comments_count": 0,
         "followers_count": 0,
         "followings_count": 0,
         "updated_at": "2018-04-06 05:39:44",
         "feeds_count": 41,
         "questions_count": 0,
         "answers_count": 0,
         "checkin_count": 0,
         "last_checkin_count": 0
     }
 }
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|name|string		|yes		   |用户昵称  |
|avatar|string		|yes		   |用户头像地址  |

## 钱包流水记录

`api/v2/tbm/org/list`

## 请求方法

`get `

## 请求体

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| type    | int      | no       |  记录类型 1;收入 -1：支出|
| state    | int      | no       |  记录状态 0：等待 1：完成 -1：失败|
| start_time    | string      | no       |  开始时间|
| end_time    | string      | no       |  结束时间|


### HTTP Status Code

200

## 返回体

```json5
 {
     "current_page": 1,
     "data": [
         {
             "id": 55,
             "owner_id": 3,
             "target_type": "transfer",
             "target_id": "2",
             "title": "转账给客户看看",
             "body": null,
             "type": -1,
             "amount": 20,
             "state": 1,
             "created_at": "2018-04-07 08:12:49",
             "updated_at": "2018-04-07 08:12:49"
         },
         {
             "id": 53,
             "owner_id": 3,
             "target_type": "transfer",
             "target_id": "2",
             "title": "转账给客户看看",
             "body": null,
             "type": -1,
             "amount": 20,
             "state": 1,
             "created_at": "2018-04-07 08:12:48",
             "updated_at": "2018-04-07 08:12:48"
         },
         {
             "id": 45,
             "owner_id": 3,
             "target_type": "transfer",
             "target_id": "2",
             "title": "转账给客户看看",
             "body": null,
             "type": -1,
             "amount": 20,
             "state": 1,
             "created_at": "2018-04-07 08:12:44",
             "updated_at": "2018-04-07 08:12:44"
         }
     ],
     "first_page_url": "http://www.tbm.com/api/v2/tbm/wallet/list?page=1",
     "from": 1,
     "last_page": 4,
     "last_page_url": "http://www.tbm.com/api/v2/tbm/wallet/list?page=4",
     "next_page_url": "http://www.tbm.com/api/v2/tbm/wallet/list?page=2",
     "path": "http://www.tbm.com/api/v2/tbm/wallet/list",
     "per_page": 7,
     "prev_page_url": null,
     "to": 7,
     "total": 27
 }
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|id|int		|yes		   |记录ID  |
|owner_id|int		|yes		   |用户ID  |
|target_type|int		|yes		   |流水类型  |
|target_id|int		|yes		   |目标ID  |
|title|string		|yes		   |标题  |
|body|string		|yes		   |内容  |
|type|int		|yes		   |分类  1：收入 -1：支出|
|amount|int		|yes		   |金额  |
|state|int		|yes		   |记录状态 0：等待 1：完成 -1：失败  |
|current_page|int		|yes		   |当前页  |
|first_page_url|string		|yes		   |第一页url  |
|last_page_url|string		|yes		   |最后一页url  |
|next_page_url|string		|yes		   |下一页url  |
|total|int		|yes		   |数据条数 |
