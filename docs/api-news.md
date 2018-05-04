# 资讯

## 获取资讯列表

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| limit   | int  | 条目数 |
| cate_id | int | 分类id |
| key | string | 关键词 |
| type | string | top-头条资讯 follow-关注机构资讯 默认top|
| after | int | 翻页表示 |
| user_id | int | 用户ID |
```
GET /tbm/news
```
### 响应
```
status 200
```
```json
[
     {
        "id": 15,
        "title": "222", // 资讯标题
        "storage": null,
        "digg_count": 0,
        "comment_count": 0,
        "hits": 0,
        "from": "原创",//
        "is_recommend": 0,
        "subject": null,
        "author": "183****4307",
        "audit_status": 2,
        "audit_count": 0,
        "user_id": 6,
        "cate_id": 1,
        "contribute_amount": 0,
        "text_content": null,
        "created_at": "2018-03-20 09:52:08",
        "updated_at": "2018-03-20 09:52:08",
        "deleted_at": null,
        "comment_status": 0,
        "has_collect": false,
        "share_count": 10,
        "has_like": false,
        "count": 0,
        "category": {
            "id": 1,
            "name": "TBMARK",
            "rank": 0,
            "created_at": null,
            "updated_at": null
        },
        "image": null,
        "pinned": null
     }
]
```
### 返回参数

| 名称 | 类型 | 说明 |
|:----:|:----:|------|
| id   | int  | 数据id |
| title | string | 资讯标题 |
| subject | string | 摘要 |
| from | string | 来源 |
| author | string | 作者 |
| user_id | int | 发布者id |
| hits | int  | 点击数 |
| has_collect | bool | 当前用户是否已收藏 |
| comment_count | bool | 评论数 |
| has_like | bool | 当前用户是否已点赞 |
| category | array | 所属分类信息 |
| category.id | int | 所属分类id |
| category.name | string | 所属分类名称 |
| category.rank | int | 所属分类排序 |
| image | array/null | 资讯封面信息 为null时表示该资讯无缩略图|
| image.id | int | 资讯封面附件id |
| image.size | string | 资讯封面尺寸 |
| comment_status | int | 是否开启评论:1-开启0-关闭 |
| share_count | int | 分享数 |

## 发布资讯(机构用户使用)

### 参数
| 字段 | 类型 | 描述 |
|:----:|:----:|----|
| title | String | **必须**，标题，最长 20 个字。 |
| subject | String | **必须** 主题，摘要，概述，最长 200 个字。 |
| content | String | **必须**，内容。 |
| image | Integer | **必须** 缩略图。 |
| tags | string,array | **必须** 标签id，多个id以逗号隔开或传入数组形式 |
|audit_status| Integer| **必须** 0-普通 上头条-1 5-草稿箱|
| from | String | 资讯来源。 |
| author | String | 作者 |
| comment_status | int | 1-资讯可评论 0-资讯不能评论 |
### 补充说明
`
audit_status为3代表上头条资讯被驳回，可以进行修改编辑
`
```
POST /tbm/news
```
### 响应
```
status 200
```
```json
{
    "message": "发布资讯成功"
}
```
## 修改资讯(机构后台使用)

### 参数
| 字段 | 类型 | 描述 |
|:----:|:----:|----|
| title | String | 标题，最长 20 个字。 |
| subject | String | 主题，摘要，概述，最长 200 个字。 |
| content | String | 内容。 |
| image | Integer | 缩略图。 |
| tags | string,array | 标签id，多个id以逗号隔开或传入数组形式 |
|audit_status| Integer| 0-普通 上头条-1 5-草稿箱|
| from | String | 资讯来源。 |
| author | String | 作者 |
| comment_status | int | 1-资讯可评论 0-资讯不能评论 |
### 补充说明
`
audit_status为3代表上头条资讯被驳回，可以进行修改编辑
`
## 删除评论(机构后台使用)
```
delete /tbm/comments/:comment
```
### 响应
```
status 204
```
## 设置评论显示状态(机构后台使用)
```
patch /tbm/comments/:comment/show
```
### 响应
```
status 204
```

