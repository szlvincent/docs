# 绑定邀请码 API 文档

## 绑定邀请码

`api/v2/tbm/invite`

## 请求方法

`post `

## 请求体
| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| user_id    | int      | yes       |  邀请码 （邀请人ID）  |

### HTTP Status Code

201

## 返回体

```json5
{
    "message": "绑定成功"
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| message    | string      | yes       |  描述信息  |



