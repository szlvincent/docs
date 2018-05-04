# 糖果分类API

## 获取所有糖果分类


### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| cate_name   | string  | 可选,  糖果分类名称|
```
get /tbm/candy_cate/list
```
### HTTP Status Code

200

## 返回体

```json5
[
    {
        "id": 1,
        "cat_name": "公交卡",
        "logo": 89,
        "mark": "也看看",
        "state": 1,
        "status": 0,
        "created_at": "2018-04-18 02:02:36",
        "updated_at": "2018-04-18 02:02:36"
    },
    {
        "id": 2,
        "cat_name": "电脑机房价格",
        "logo": 90,
        "mark": "滏东嘉园看见了",
        "state": 1,
        "status": 0,
        "created_at": "2018-04-18 02:42:53",
        "updated_at": "2018-04-18 02:42:53"
    },
    {
        "id": 3,
        "cat_name": "考虑",
        "logo": 91,
        "mark": "等忙过格列美脲飞比较",
        "state": 1,
        "status": 0,
        "created_at": "2018-04-18 02:55:09",
        "updated_at": "2018-04-18 02:55:09"
    }
]
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| id    | int      | yes       |  分类ID  |
| cat_name    | string      | yes       |  分类名称  |
| logo    | int      | yes       |  LOGO ID  |
| mark    | string      | yes       |  糖果介绍  |
| state    | int      | yes       |  是否前台可见 0：不可见1：可见  |
| status    | int      | yes       |  是否开启提现 0：关闭1：开启  |

## 添加分类

## 请求体
| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| cat_name    | string      | yes       |  分类名称  |
| logo    | int      | yes       |  LOGO 图片ID  |
| mark    | int      | yes       |  糖果分类介绍  |

```
POST /tbm/candy_cate
```
### 响应
```
status 201 
```
## 返回体

```json5
{
    "cat_name": "公交卡1234",
    "logo": "86",
    "mark": "这个是简介",
    "state": 0,
    "status": 0,
    "updated_at": "2018-04-18 06:39:27",
    "created_at": "2018-04-18 06:39:27",
    "id": 5
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| id    | int      | yes       |  分类ID  |
| cat_name    | string      | yes       |  分类名称  |
| logo    | int      | yes       |  LOGO ID  |
| mark    | string      | yes       |  糖果介绍  |
| state    | int      | yes       |  是否前台可见 0：不可见1：可见  |
| status    | int      | yes       |  是否开启提现 0：关闭1：开启  |

## 判断该分类名称是否存在
如果存在直接返回该分类的信息，不存在返回404 {"message": "分类不存在"}

## 请求体
| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| cate_name    | string      | yes       |  分类名称  |

```
get /tbm/candy_cate/exists
```
### 响应
```
status 200 
```
## 返回体

```json5
{
    "id": 5,
    "cat_name": "公交卡1234",
    "logo": 86,
    "mark": "这个是简介",
    "state": 0,
    "status": 0,
    "created_at": "2018-04-18 06:39:27",
    "updated_at": "2018-04-18 06:39:27"
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| id    | int      | yes       |  分类ID  |
| cat_name    | string      | yes       |  分类名称  |
| logo    | int      | yes       |  LOGO ID  |
| mark    | string      | yes       |  糖果介绍  |
| state    | int      | yes       |  是否前台可见 0：不可见1：可见  |
| status    | int      | yes       |  是否开启提现 0：关闭1：开启  |