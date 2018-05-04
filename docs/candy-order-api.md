# 兑换糖果API

## 参与糖果兑换

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| tbmark   | int  | 必须, 参与TBMark 值|
| candy_id | int | 必须, 糖果任务ID |
```
POST /tbm/candy_order
```
### HTTP Status Code

201

## 返回体

```json5
{
    "id": 1,
    "user_id": 3,
    "candy_id": 1,
    "name": "公交卡卡卡",
    "cost": 4000,
    "candy_num": "0.00000000",
    "status": 0,
    "created_at": "2018-04-18 07:18:04",
    "updated_at": "2018-04-18 07:28:05",
    "user": {
        "id": 3,
        "name": "hello",
        "email": null,
        "bio": null,
        "sex": 0,
        "location": null,
        "created_at": "2018-03-21 02:22:17",
        "updated_at": "2018-04-15 12:32:18",
        "rank_status": 1,
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
        }
    }
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|id|int		|yes		   |记录ID  |
|user_id|int		|yes		   |用户ID  |
|candy_id|int		|yes		   |糖果任务ID  |
|name|string		|yes		   |糖果名称  |
|cost|int		|yes		   |参与总TBMark值  |
|candy_num|float		|yes		   |获得糖果数量  |
|status|int		|yes		   |是否兑换糖果：0：未兑换 1：已兑换  |
|user|array		|yes		   |用户信息  |
