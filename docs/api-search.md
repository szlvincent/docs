# 绑定邀请码 API 文档

## 绑定邀请码

`api/v2/tbm/search/user`

## 请求方法

`get `

## 请求体
| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| user    | string      | yes       |  用户名模糊匹配  |
| type    | string      | yes       |  group-机构用户搜索 personal-个人用户搜索  |
| limit    | int      | no       |  条目数 默认15  |
| offset    | int      | no       | 翻页标示 默认0 |

### HTTP Status Code

201

## 返回体

```json5
[
    {
        "id": 8,
        "name": "测试用户5",
        "bio": null,
        "sex": 0,
        "location": null,
        "follower": false,//是否关注他false否true是
        "created_at": "2018-02-26 08:05:00",
        "updated_at": "2018-02-26 08:05:00",
        "rank_status": 1,
        "avatar": null,
        "bg": null,
        "verified": null,
        "extra": null
    }
]
```



