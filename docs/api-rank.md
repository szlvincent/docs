# 排行

## 总排行

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| limit   | int  | 条目数 |
| offset | int | 翻页表示 |

```
GET /tbm/user/ranks
```
### 响应
```
status 200
```
```json
[
    {
        "id": 2,
        "name": "zhangsan",// 用户名
        "bio": null,
        "sex": 0,
        "location": null,
        "created_at": "2018-02-26 08:05:00",
        "updated_at": "2018-02-26 08:05:00",
        "avatar": null,
        "bg": null,
        "verified": null,
        "extra": {
            "user_id": 2,
            "likes_count": 0,
            "comments_count": 0,
            "followers_count": 0,
            "followings_count": 0,
            "invite_count": 0, // 邀请好友数
            "updated_at": "2018-02-28 13:47:38",
            "feeds_count": 0,
            "questions_count": 0,
            "answers_count": 0,
            "checkin_count": 12,
            "last_checkin_count": 1,
            "tb_mark_count": 11, // tb mark 总数
            "rank": 1 // 排名名次
        }
    }
]
```
## 好友贡献排行
```
GET /tbm/friend/contribution/ranks
```
### 参数

| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| limit   | int  | 条目数 |
| offset | int | 翻页标示 |
| type | string | 默认: all, all-累计贡献排行 day-日贡献排行 |

### 响应
```
status 200
```
```json
[
    {
        "user_id": 3,// 用户id
        "invite_id": 2,// 邀请者id
        "obtain": 0,// 贡献值
        "rank": 1, // 排名
        "inviter": {// 邀请人信息
            "id": 2,
            "name": "zhangsan",
            "bio": null,
            "sex": 0,
            "location": null,
            "created_at": "2018-02-26 08:05:00",
            "updated_at": "2018-02-26 08:05:00",
            "avatar": null,
            "bg": null,
            "verified": null,
            "extra": {
                "user_id": 2,
                "likes_count": 0,
                "comments_count": 0,
                "followers_count": 0,
                "followings_count": 0,
                "invite_count": 2,
                "updated_at": "2018-02-28 13:47:38",
                "feeds_count": 0,
                "questions_count": 0,
                "answers_count": 0,
                "checkin_count": 12,
                "last_checkin_count": 1
            }
        }
    }
]
```
