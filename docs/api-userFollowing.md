# 用户关注的机构 API 文档

## 获取用户关注的机构

`api/v2/tbm/user/following`

## 请求方法

`get `

## 请求体

无

### HTTP Status Code

200

## 返回体

```json5
{
    "V": [
        {
            "id": 2,
            "name": "Vincent",
            "bio": null,
            "sex": 0,
            "location": null,
            "created_at": "2018-03-20 07:22:00",
            "updated_at": "2018-03-22 09:25:37",
            "rank_status": 1,
            "avatar": "http://www.tbm.com/api/v2/users/2/avatar",
            "bg": null,
            "verified": {
                "type": "project_party",
                "icon": null
            },
            "extra": {
                "user_id": 2,
                "likes_count": 0,
                "comments_count": 0,
                "followers_count": 0,
                "followings_count": 0,
                "updated_at": "2018-03-21 07:46:02",
                "feeds_count": 3,
                "questions_count": 0,
                "answers_count": 0,
                "checkin_count": 0,
                "last_checkin_count": 0
            },
            "pin": "V"
        }
    ],
    "Z": [
        {
            "id": 4,
            "name": "这个很难",
            "bio": null,
            "sex": 0,
            "location": null,
            "created_at": "2018-03-22 07:41:12",
            "updated_at": "2018-03-22 07:41:12",
            "rank_status": 1,
            "avatar": null,
            "bg": null,
            "verified": null,
            "extra": null,
            "pin": "Z"
        }
    ]
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|name|string		|yes		   |主体名称  |
