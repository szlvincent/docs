# 糖果钱包API文档

## 获取我的糖果钱包


### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| limit   | int  | 非必须, 每页条数|
| offset | int | 非必须, 翻页标示 |
```
GET /tbm/candy_wallet
```
### 响应
```
status 200
```
## 返回体

```json5
[
    {
        "id": 1,
        "user_id": 3,
        "candy_cat_id": 2,
        "count": "12.00000000",
        "created_at": "2018-04-18 17:27:11",
        "updated_at": "2018-04-18 17:27:14",
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
    }
]
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| id    | int      | yes       |  记录ID  |
| user_id    | int      | yes       |  用户ID  |
| candy_cat_id    | int      | yes       |  糖果分类ID  |
| count    | float      | yes       |  糖果个数  |
| candy_cate    | array      | yes       |  糖果分类信息  |

## 获取某糖果流水


### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| candy_cat_id   | int  | 必须, 糖果分类ID|
| limit   | int  | 非必须, 每页条数|
| offset | int | 非必须, 翻页标示 |
```
GET /tbm/candy_wallet_order
```
### 响应
```
status 200
```
## 返回体

```json5
[
    {
        "id": 1,
        "title": "兑换获得BTP",
        "candy_cat_id": 2,
        "count": "12.00000000",
        "charge": "0.00000000",
        "type": 1,
        "status": 2,
        "created_at": "2018-04-18 17:43:26",
        "updated_at": "2018-04-18 17:43:29"
    }
]
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| id    | int      | yes       |  记录ID  |
| title    | string      | yes       |  说明  |
| candy_cat_id    | int      | yes       |  糖果分类ID  |
| count    | float      | yes       |  糖果个数  |
| charge    | float      | yes       |  手续费  |
| type    | int      | yes       |  类型 1：收入 2：支出  |
| status    | int      | yes       |  状态 1：等待 2：成功 3：失败  |

## 获取某糖果冻结

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| candy_cat_id   | int  | 必须, 糖果分类ID|
```
GET /tbm/candy_frozen
```
### 响应
```
status 200
```
## 返回体

```json5
{
    "available": "0",
    "unavailable": "19.00000000"
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| available    | float      | yes       |  可用数量  |
| unavailable    | float      | yes       |  冻结数量  |

## 获取我的TBMark冻结

### 参数
无
```
GET /tbm/mark_frozen
```
### 响应
```
status 200
```
## 返回体

```json5
{
    "available": 460,
    "unavailable": 5000
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
| available    | int      | yes       |  可用数量  |
| unavailable    | int      | yes       |  冻结数量  |