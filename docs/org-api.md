# 机构 API 文档

## 获取机构信息

`api/v2/tbm/orginfo`

## 请求方法

`get `

## 请求体

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| user_id    | int      | yes       |  机构用户ID  |

### HTTP Status Code

200

## 返回体

```json5
{
    "photo": 12,
    "nickname": "vincent",
    "remarks": "makes",
    "introduce": "这个是简介",
    "other_info": "['aa':123]",
    "white_paper": 13,
    "white_paper_name": "tokenbook白皮书",
    "created_at": "2018-03-01 05:49:52",
    "updated_at": "2018-03-01 05:50:15"
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| photo    | int      | yes       |  头像文件ID  |
| nickname    | string      | yes       |  昵称  |
| remarks    | string      | yes       |  备注信息  |
| introduce    | string      | yes       |  简介  |
| other_info    | array      | yes       |  补充信息  |
| white_paper_name    | string      | yes       |  白皮书文件名称  |
| white_paper    | int      | yes       |  白皮书文件ID  |

## 发布机构信息

`api/v2/tbm/orginfo`

## 请求方法

`post `

## 请求体

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| photo    | int      | yes       |  头像文件ID  |
| nickname    | string      | yes       |  昵称  |
| remarks    | string      | yes       |  备注信息  |
| introduce    | string      | yes       |  简介  |
| other_info    | array      | yes       |  补充信息  |
| white_paper_name    | string      | yes       |  白皮书文件名称  |
| white_paper    | int      | yes       |  白皮书文件ID  |

### HTTP Status Code

201

## 返回体

```json5
 "message": [
        "编辑成功"
    ]
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|message|string		|yes		   |返回信息  |

## 更新机构信息

`api/v2/tbm/orginfo`

## 请求方法

`patch `

## 请求体

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| photo    | int      | yes       |  头像文件ID  |
| remarks    | string      | yes       |  备注信息  |
| introduce    | string      | yes       |  简介  |
| other_info    | array      | yes       |  补充信息  |
| white_paper    | int      | yes       |  白皮书文件ID  |
| white_paper_name    | string      | yes       |  白皮书文件名称 |

### HTTP Status Code

201

## 返回体

```json5
 "message": [
        "编辑成功"
    ]
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|message|string		|yes		   |返回信息  |

## 检查用户名是否可用

`api/v2/tbm/check-name`

## 请求方法

`get `

## 请求体

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| name    | string      | yes       |  昵称  |


### HTTP Status Code

201

## 返回体

```json5
 "message": ["用户名已存在" ],
 "status" : 0
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|message|string		|yes		   |返回信息  |
|status|int		|yes		   |0：不可用 1:可用  |

## 机构首页

`api/v2/tbm/org-user`

## 请求方法

`get `

## 请求体

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| type    | string      | no       |  类型 今日：today 所有：all 默认为today  |
| limit    | int      | no       |  每页个数 默认为15条  |
| offset    | int      | no       |  过滤个数 默认为0  |

### HTTP Status Code

201

## 返回体

```json5
{
    "today_followers_count": 2,
    "followers_count": 0,
    "users": [
        3,
        4
    ]
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|today_followers_count|int		|yes		   |今日关注总数  |
|followers_count|int		|yes		   |所有关注人数  |
|users|array		|yes		   |关注用户id  |

## 获取机构列表

`api/v2/tbm/org/list`

## 请求方法

`get `

## 请求体

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|limit|int		|no		   |每页条数  |
|offset|int		|no		   |偏移量  |

### HTTP Status Code

200

## 返回体

```json5
[
    {
        "photo": 12,
        "nickname": "vincent",
        "remarks": "marks",
        "introduce": "这是简介",
        "other_info": "['aa':123]",
        "white_paper": 12,
        "white_paper_name": "tokenbook白皮书",
        "created_at": "2018-03-02 19:33:33",
        "updated_at": "2018-03-02 19:33:35"
    }
]
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|photo |int		|yes		   |Logo图片 ID  |
|nickname|string		|yes		   |昵称  |
|remarks|string		|yes		   |备注  |
|introduce|string		|yes		   |简介  |
|other_info|array		|yes		   |补充信息  |
|white_paper|int		|yes		   |白皮书  |
|white_paper_name|string		|yes		   |白皮书名称  |

## 获取机构发布的快讯

`api/v2/tbm/org/news/list`

## 请求方法

`get `

## 请求体

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| orgId    | int      | yes       |  机构ID  |
| limit    | int      | no       |  每页个数 默认为15条  |
| offset    | int      | no       |  过滤个数 默认为0  |

### HTTP Status Code

200

## 返回体

```json5
[
    {
        "id": 1,
        "user_id": 2,
        "feed_content": "这个是什么啊",
        "feed_from": 1,
        "like_count": 0,
        "feed_view_count": 0,
        "feed_comment_count": 0,
        "feed_latitude": "",
        "feed_longtitude": "",
        "feed_geohash": "",
        "audit_status": 1,
        "feed_mark": 11,
        "created_at": "2018-03-01 03:00:04",
        "updated_at": "2018-03-01 03:00:04",
        "deleted_at": null,
        "images": [],
        "paid_node": null
    },
    {
        "id": 2,
        "user_id": 2,
        "feed_content": "的防空法看",
        "feed_from": 1,
        "like_count": 0,
        "feed_view_count": 0,
        "feed_comment_count": 0,
        "feed_latitude": "",
        "feed_longtitude": "",
        "feed_geohash": "",
        "audit_status": 1,
        "feed_mark": 12,
        "created_at": "2018-03-02 19:06:39",
        "updated_at": "2018-03-02 19:06:41",
        "deleted_at": null,
        "images": [],
        "paid_node": null
    }
]
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|id |int		|yes		   |记录ID  |
|feed_content|string		|yes		   |快讯内容  |
|feed_mark|int		|yes		   |唯一标识  |

## 设置机构消息置顶

`api/v2/tbm/top/org`

## 请求方法

`patch `

## 请求体

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| orgId    | int      | yes       |  机构ID  |
| is_top    | int      | yes       |  是否置顶：1-置顶 0-不置顶  |

### HTTP Status Code

201

## 返回体

```json5
{
    "id": 2,
    "user_id": 3,
    "target": 2,
    "created_at": "2018-03-22 15:50:02",
    "updated_at": "2018-03-22 15:50:05",
    "is_top": 0
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|id |int		|yes		   |记录ID  |
|user_id|int		|yes		   |用户ID  |
|target|int		|yes		   |目标用户ID  |
|is_top|int		|yes		   |当前置顶状态 1-置顶 0-不置顶  |


