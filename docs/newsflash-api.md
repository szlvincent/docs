# 发布快讯 API 文档

## 发布快讯

`api/v2/tbm/newsflash`

## 请求方法

`post `

## 请求体

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| feed_content    | string      | yes       |  快讯内容  |
| feed_mark    | int      | yes       |  唯一标记  |
| feed_from    | int      | yes       |  动态来源 1:pc 2:h5 3:ios 4:android 5:其他  |

### HTTP Status Code

201

## 返回体

```json5
{
    "message": [
        "发布成功"
    ],
    "id": 1
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|message|string		|yes		   |返回信息  |
|id|string		|yes		   |记录ID  |

## 获取快讯发布数量

`api/v2/tbm/news-flash-count`

## 请求方法

`get `

## 请求体

无

### HTTP Status Code

200

## 返回体

```json5
{
    "all_count": 30,
    "count": 0,
    "last_count": 30
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|all_count|int		|yes		   |所有可发条数  |
|count|int		|yes		   |已经发送条数  |
|last_count|int		|yes		   |剩余可发条数  |
|words|int		|yes		   |资讯可发布的字数  |
