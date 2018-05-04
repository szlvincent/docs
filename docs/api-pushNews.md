# 获取关注机构历史快讯和咨询 API 文档

## 获取历史记录

`api/v2/tbm/push/news`

## 请求方法

`get `

## 请求体

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|orgId|int		|yes		   |机构用户ID  |
|feedAfter|int		|yes		   | 快讯最小ID  |
|newsAfter|int		|yes		   | 咨询最小ID  |
|limit|int		|yes		   | 分别获取条数 默认为8  |

### HTTP Status Code

200

## 返回体

```json5
{
    "data": [
        {
            "id": 1,
            "title": "fhfjng",
            "content": "gkljl",
            "digg_count": 0,
            "comment_count": 0,
            "hits": 0,
            "from": null,
            "is_recommend": 0,
            "subject": null,
            "author": "2",
            "audit_status": 0,
            "audit_count": 0,
            "user_id": 2,
            "contribute_amount": 0,
            "text_content": null,
            "created_at": "2018-03-22 18:22:55",
            "updated_at": "2018-03-22 18:22:58",
            "comment_status": 1,
            "type": "news",
            "category": null,
            "image": {
                "id": 1,
                "size": "500x332"
            },
            "pinned": null
        },
        {
            "id": 3,
            "user_id": 2,
            "feed_content": "二氧化碳加油卡",
            "feed_from": 1,
            "like_count": 0,
            "feed_view_count": 0,
            "feed_comment_count": 0,
            "feed_latitude": "",
            "feed_longtitude": "",
            "feed_geohash": "",
            "audit_status": 2,
            "feed_mark": 1521618362467,
            "created_at": "2018-03-21 07:46:02",
            "updated_at": "2018-03-21 07:46:02",
            "deleted_at": null,
            "share_count": 0,
            "can_comment": 1,
            "type": "feed",
            "images": [],
            "paid_node": null
        },
        {
            "id": 2,
            "user_id": 2,
            "feed_content": "老人们和南方女孩",
            "feed_from": 1,
            "like_count": 0,
            "feed_view_count": 0,
            "feed_comment_count": 0,
            "feed_latitude": "",
            "feed_longtitude": "",
            "feed_geohash": "",
            "audit_status": 1,
            "feed_mark": 1521540897505,
            "created_at": "2018-03-20 10:14:57",
            "updated_at": "2018-03-20 10:14:57",
            "deleted_at": null,
            "share_count": 0,
            "can_comment": 1,
            "type": "feed",
            "images": [],
            "paid_node": null
        }
    ],
    "feedMin": 2,
    "newsMin": 1
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|data|object		|yes		   |主体名称  |
|feedMin|int		|yes		   |快讯最小ID  |
|newsMin|int		|yes		   |咨询最小ID  |
