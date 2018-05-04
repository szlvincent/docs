# 糖果相关API

## 机构用户发布糖果计划

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| name   | string  | 必须, 糖果名称|
| candy_cat_id | int | 必须, 糖果分类ID |
| candy_num | int | 必须, 糖果发放数量 |
| time_line | int | 必须, 糖果任务时长 |
| prject_name | string | 必须, 项目名称 |
| prject_desc | string | 必须, 项目介绍 |
| link | string | 必须, 官网地址 |
| link | string | 必须, 官网地址 |
| exchange_link | string | 可选, 交易所地址 |
```
POST /tbm/candy
```
### HTTP Status Code

201

## 返回体

```json5
{
    "message": [
        "糖果任务发布成功，请及时充值糖果"
    ]
}
`````

## 充值糖果开启审核


### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| receipt   | int  | 必须, 回执图片ID|
```
patch /tbm/candy/{candy}
```
### HTTP Status Code

201

## 返回体

```json5
{
    "id": 1,
    "candy_id": "201804180338156193",
    "candy_cat_id": 1,
    "name": "公交卡",
    "receipt_pic": "89",
    "candy_num": 100,
    "time_line": 10,
    "start_at": null,
    "end_at": null,
    "data": {
        "prject_name": "这个很牛逼",
        "prject_desc": "这个牛逼的不行"
        "link": "www.baidu.com"
    },
    "status": 1,
    "created_at": "2018-04-18 03:38:15",
    "updated_at": "2018-04-18 03:49:14",
    "candy_cate": {
        "id": 1,
        "cat_name": "公交卡",
        "logo": 89,
        "mark": "也看看",
        "state": 1,
        "status": 0,
        "created_at": "2018-04-18 02:02:36",
        "updated_at": "2018-04-18 02:02:36"
    }
}
`````
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| id    | int      | yes       |  用户ID  |
| candy_id    | string      | yes       |  糖果任务ID  |
| candy_cat_id    | int      | yes       |  分类ID  |
| name    | string      | yes       |  糖果名称  |
| receipt_pic    | int      | yes       |  回执截图ID  |
| candy_num    | int      | yes       |  糖果数量  |
| time_line    | int      | yes       |  活动时长  |
| start_at    | string      | yes       |  开始时间：以审核时间为准  |
| end_at    | string      | yes       |  结束时间：以审核时间 + 活动时长  |
| status    | int      | yes       |  活动状态： 0：未启动 1：待审核 2：开启3：结束 |
| data    | array      | yes       |  项目推广信息  |
| prject_name    | string      | yes       |  项目名称  |
| prject_desc    | string      | yes       |  项目描述 |
| link    | string      | yes       |  官网地址 |
| candy_cate    | array      | yes       |  糖果分类信息 |
| id    | int      | yes       |  糖果分类ID |
| cat_name  | string      | yes       |  糖果分类名称 |
| logo  | int       | yes       |  糖果分类LOGO |
| mark  | string       | yes       |  糖果分类介绍 |
| state  | int       | yes       | 是否前台可见 0：不可见1：可见 |
| status  | int       | yes       | 是否开启提现 0：不可提现1：可提现 |

## 更新糖果任务


### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| name   | string  | 必须, 糖果名称|
| candy_cat_id | int | 必须, 糖果分类ID |
| candy_num | int | 必须, 糖果发放数量 |
| time_line | int | 必须, 糖果任务时长 |
| prject_name | string | 必须, 项目名称 |
| prject_desc | string | 必须, 项目介绍 |
| link | string | 必须, 官网地址 |
| link | string | 必须, 官网地址 |
| exchange_link | string | 可选, 交易所地址 |
```
patch /tbm/update-candy/{candy}
```
### HTTP Status Code

201

## 返回体

```json5
{
    "id": 1,
    "candy_id": "201804180338156193",
    "candy_cat_id": "3",
    "name": "公交卡卡卡",
    "receipt_pic": 89,
    "candy_num": "200",
    "time_line": "15",
    "start_at": null,
    "end_at": null,
    "data": {
        "prject_name": "哈哈哈",
        "prject_desc": "这个是尿素",
        "link": "www.baidu.com"
    },
    "status": 0,
    "created_at": "2018-04-18 03:38:15",
    "updated_at": "2018-04-18 04:44:43",
    "candy_cate": {
        "id": 3,
        "cat_name": "考虑",
        "logo": 91,
        "mark": "等忙过格列美脲飞比较",
        "state": 1,
        "status": 0,
        "created_at": "2018-04-18 02:55:09",
        "updated_at": "2018-04-18 02:55:09"
    }
}
`````
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| id    | int      | yes       |  用户ID  |
| candy_id    | string      | yes       |  糖果任务ID  |
| candy_cat_id    | int      | yes       |  分类ID  |
| name    | string      | yes       |  糖果名称  |
| receipt_pic    | int      | yes       |  回执截图ID  |
| candy_num    | int      | yes       |  糖果数量  |
| time_line    | int      | yes       |  活动时长  |
| start_at    | string      | yes       |  开始时间：以审核时间为准  |
| end_at    | string      | yes       |  结束时间：以审核时间 + 活动时长  |
| status    | int      | yes       |  活动状态： 0：未启动 1：待审核 2：开启3：结束 |
| data    | array      | yes       |  项目推广信息  |
| prject_name    | string      | yes       |  项目名称  |
| prject_desc    | string      | yes       |  项目描述 |
| link    | string      | yes       |  官网地址 |
| candy_cate    | array      | yes       |  糖果分类信息 |
| id    | int      | yes       |  糖果分类ID |
| cat_name  | string      | yes       |  糖果分类名称 |
| logo  | int       | yes       |  糖果分类LOGO |
| mark  | string       | yes       |  糖果分类介绍 |
| state  | int       | yes       | 是否前台可见 0：不可见1：可见 |
| status  | int       | yes       | 是否开启提现 0：不可提现1：可提现 |

## 机构获取糖果任务列表


### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| key   | string  | 可选, 糖果名称或者项目名称|
| size   | int  | 可选, 分页条数。默认是8条|
| status | int | 可选, 糖果任务状态 0：未开始 1：审核中 2：进行中 3：已结束 |
```
get /tbm/candy/list
```
### HTTP Status Code

200

## 返回体

```json5
{
    "current_page": 1,
    "data": [
        {
            "id": 2,
            "candy_id": "201804180338156192",
            "candy_cat_id": 2,
            "name": "公交卡卡",
            "receipt_pic": 89,
            "candy_num": 100,
            "time_line": 12,
            "start_at": "2018-04-18 16:05:41",
            "end_at": "2018-04-19 04:05:41",
            "data": {
                "prject_name": "哈哈哈",
                "prject_desc": "这个是尿素",
                "link": "www.baidu.com"
            },
            "status": 3,
            "created_at": null,
            "updated_at": "2018-04-18 16:05:41",
            "tbmark": 0,
            "candy_cate": {
                "id": 2,
                "cat_name": "电脑机房价格",
                "logo": 90,
                "mark": "滏东嘉园看见了",
                "state": 1,
                "status": 0,
                "created_at": "2018-04-18 02:42:53",
                "updated_at": "2018-04-18 02:42:53"
            }
        },
        {
            "id": 1,
            "candy_id": "201804180338156193",
            "candy_cat_id": 3,
            "name": "公交卡卡卡",
            "receipt_pic": 89,
            "candy_num": 200,
            "time_line": 15,
            "start_at": "2018-04-18 12:53:38",
            "end_at": "2018-04-18 22:53:44",
            "data": {
                "prject_name": "哈哈哈",
                "prject_desc": "这个是尿素",
                "link": "www.baidu.com"
            },
            "status": 2,
            "created_at": "2018-04-18 03:38:15",
            "updated_at": "2018-04-18 04:58:02",
            "tbmark": "4000",
            "candy_cate": {
                "id": 3,
                "cat_name": "考虑",
                "logo": 91,
                "mark": "等忙过格列美脲飞比较",
                "state": 1,
                "status": 0,
                "created_at": "2018-04-18 02:55:09",
                "updated_at": "2018-04-18 02:55:09"
            }
        }
    ],
    "first_page_url": "http://www.tbm.com/api/v2/tbm/candy/list?page=1",
    "from": 1,
    "last_page": 1,
    "last_page_url": "http://www.tbm.com/api/v2/tbm/candy/list?page=1",
    "next_page_url": null,
    "path": "http://www.tbm.com/api/v2/tbm/candy/list",
    "per_page": 8,
    "prev_page_url": null,
    "to": 2,
    "total": 2,
    "not_begin": 0,
    "has_begin": 1,
    "end": 1
}
`````
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| id    | int      | yes       |  用户ID  |
| candy_id    | string      | yes       |  糖果任务ID  |
| candy_cat_id    | int      | yes       |  分类ID  |
| name    | string      | yes       |  糖果名称  |
| receipt_pic    | int      | yes       |  回执截图ID  |
| candy_num    | int      | yes       |  糖果数量  |
| time_line    | int      | yes       |  活动时长  |
| start_at    | string      | yes       |  开始时间：以审核时间为准  |
| end_at    | string      | yes       |  结束时间：以审核时间 + 活动时长  |
| status    | int      | yes       |  活动状态： 0：未启动 1：待审核 2：开启3：结束 |
| data    | array      | yes       |  项目推广信息  |
| prject_name    | string      | yes       |  项目名称  |
| prject_desc    | string      | yes       |  项目描述 |
| link    | string      | yes       |  官网地址 |
| candy_cate    | array      | yes       |  糖果分类信息 |
| id    | int      | yes       |  糖果分类ID |
| cat_name  | string      | yes       |  糖果分类名称 |
| logo  | int       | yes       |  糖果分类LOGO |
| mark  | string       | yes       |  糖果分类介绍 |
| state  | int       | yes       | 是否前台可见 0：不可见1：可见 |
| status  | int       | yes       | 是否开启提现 0：不可提现1：可提现 |
| not_begin  | int       | yes       | 未开始 |
| has_begin  | int       | yes       | 进行中 |
| end  | int       | yes       | 已结束 |

## APP获取糖果任务列表

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| limit   | int  | 可选, 分页条数。默认是15条|
| page   | int  | 可选, 翻页标识。当前页码。默认为1|
```
get /tbm/app-candy/list
```
### HTTP Status Code

200

## 返回体

```json5
[
    {
        "id": 1,
        "candy_id": "201804180338156193",
        "candy_cat_id": 3,
        "name": "公交卡卡卡",
        "receipt_pic": 89,
        "candy_num": 200,
        "time_line": 15,
        "start_at": "2018-04-18 12:53:38",
        "end_at": "2018-04-18 22:53:44",
        "data": {
            "prject_name": "哈哈哈",
            "prject_desc": "这个是尿素",
            "link": "www.baidu.com"
        },
        "status": 2,
        "created_at": "2018-04-18 03:38:15",
        "updated_at": "2018-04-18 04:58:02",
        "tbmark": 0,
        "total_tbmark": 0,
        "end_sec": 64345,
        "candy_cate": {
            "id": 3,
            "cat_name": "考虑",
            "logo": 91,
            "mark": "等忙过格列美脲飞比较",
            "state": 1,
            "status": 0,
            "created_at": "2018-04-18 02:55:09",
            "updated_at": "2018-04-18 02:55:09"
        }
    }
]
`````
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| id    | int      | yes       |  糖果记录ID  |
| user_id    | int      | yes       |  用户ID  |
| candy_id    | string      | yes       |  糖果任务ID  |
| candy_cat_id    | int      | yes       |  分类ID  |
| name    | string      | yes       |  糖果名称  |
| receipt_pic    | int      | yes       |  回执截图ID  |
| candy_num    | int      | yes       |  糖果数量  |
| time_line    | int      | yes       |  活动时长  |
| start_at    | string      | yes       |  开始时间：以审核时间为准  |
| end_at    | string      | yes       |  结束时间：以审核时间 + 活动时长  |
| status    | int      | yes       |  活动状态： 0：未启动 1：待审核 2：开启3：结束 |
| tbmark    | int      | yes       |  我参与的TBMark值  |
| total_tbmark    | int      | yes       |  所有TBMark值  |
| end_sec    | int      | yes       |  距离结束还有多少秒  |
| data    | array      | yes       |  项目推广信息  |
| prject_name    | string      | yes       |  项目名称  |
| prject_desc    | string      | yes       |  项目描述 |
| link    | string      | yes       |  官网地址 |
| candy_cate    | array      | yes       |  糖果分类信息 |
| id    | int      | yes       |  糖果分类ID |
| cat_name  | string      | yes       |  糖果分类名称 |
| logo  | int       | yes       |  糖果分类LOGO |
| mark  | string       | yes       |  糖果分类介绍 |
| state  | int       | yes       | 是否前台可见 0：不可见1：可见 |
| status  | int       | yes       | 是否开启提现 0：不可提现1：可提现 |

## 获取某个糖果任务详情


### 参数
无
```
get /tbm/candy/{candy}
```
### HTTP Status Code

200

## 返回体

```json5
{
    "id": 1,
    "candy_id": "201804180338156193",
    "candy_cat_id": 3,
    "name": "公交卡卡卡",
    "receipt_pic": 89,
    "candy_num": 200,
    "time_line": 15,
    "start_at": "2018-04-18 12:53:38",
    "end_at": "2018-04-18 22:53:44",
    "data": {
        "prject_name": "哈哈哈",
        "prject_desc": "这个是尿素",
        "link": "www.baidu.com"
    },
    "status": 2,
    "created_at": "2018-04-18 03:38:15",
    "updated_at": "2018-04-18 04:58:02",
    "total_tbmark": 0,
    "candy_cate": {
        "id": 3,
        "cat_name": "考虑",
        "logo": 91,
        "mark": "等忙过格列美脲飞比较",
        "state": 1,
        "status": 0,
        "created_at": "2018-04-18 02:55:09",
        "updated_at": "2018-04-18 02:55:09"
    }
}
`````
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| id    | int      | yes       |  糖果记录ID  |
| user_id   | int      | yes       |  用户ID  |
| candy_id    | string      | yes       |  糖果任务ID  |
| candy_cat_id    | int      | yes       |  分类ID  |
| name    | string      | yes       |  糖果名称  |
| receipt_pic    | int      | yes       |  回执截图ID  |
| candy_num    | int      | yes       |  糖果数量  |
| time_line    | int      | yes       |  活动时长  |
| start_at    | string      | yes       |  开始时间：以审核时间为准  |
| end_at    | string      | yes       |  结束时间：以审核时间 + 活动时长  |
| status    | int      | yes       |  活动状态： 0：未启动 1：待审核 2：开启3：结束 |
| total_tbmark    | int      | yes       |  所有TBMark值  |
| data    | array      | yes       |  项目推广信息  |
| prject_name    | string      | yes       |  项目名称  |
| prject_desc    | string      | yes       |  项目描述 |
| link    | string      | yes       |  官网地址 |
| candy_cate    | array      | yes       |  糖果分类信息 |
| id    | int      | yes       |  糖果分类ID |
| cat_name  | string      | yes       |  糖果分类名称 |
| logo  | int       | yes       |  糖果分类LOGO |
| mark  | string       | yes       |  糖果分类介绍 |
| state  | int       | yes       | 是否前台可见 0：不可见1：可见 |
| status  | int       | yes       | 是否开启提现 0：不可提现1：可提现 |

## 删除未开始的糖果任务


### 参数
无
```
delete /tbm/candy/{candy}
```
### HTTP Status Code

204

## 返回体

null