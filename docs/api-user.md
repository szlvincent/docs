# 用户相关接口

## 个人中心
```
GET /tbm/user
```
### 响应
```
status 200 
```
```json
{
    "id": 2,
    "name": "zhangsan",
    "bio": null,
    "sex": 0,
    "location": null,
    "created_at": "2018-02-26 08:05:00",
    "updated_at": "2018-02-26 08:05:00",
    "rank_status": 1, // 1参与排行 0不参与
    "checkin": {
        "check_in_status": false,// 今日是否签到
        "check_in_reward": 1 // 签到奖励
    },
    "newWallet": {// 钱包
        "owner_id": 2,
        "balance": 0, // tbmark 数量.
        "total_income": 0,
        "total_expenses": 0,
        "created_at": "2018-03-02 03:17:55",
        "updated_at": "2018-03-02 03:17:55"
    },
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
        "checkin_count": 12, // 用户签到统计.
        "last_checkin_count": 1, // 用户连续签到统计.
        "user_rank": 5,// 当前排名 按照tbmark数量排行.
        "friend_count": 0 // 好友数量
    }
}
```
## 参与排行
```
POST /tbm/user/rank/status
```
### 响应
```
status 204
```
## 获取参与排行状态
```
GET /tbm/user/rank/status
```
### 响应
```
status 200
```
```json
{
    "status": 0
}
```