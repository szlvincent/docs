# 积分商城API

## 竞拍商品

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| limit   | int  | 一页显示多少个|
| offset | int | maxSize |

```
GET /api/v2/auction/index
```
### HTTP Status Code

200

## 返回体

```json5
[
    {
        "id": 1,
        "goods_id": 1,
        "auction_title": "活动——1",
        "auction_content": "活动——1",
        "auction_scale": "0.01",
        "auction_price": "100.00000000",
        "auction_stock": 1,
        "auction_count": 6,
        "candy_cat_id": 1,
        "start_time": "2018-05-03 15:07:51",
        "end_time": "2018-05-03 18:01:10",
        "created_at": "2018-05-03 15:07:49",
        "updated_at": "2018-05-05 14:47:07",
        "picture": 4,
        "maxPrice": "455.00000000",
        "status": 3,
        "time_line": -1
    },
    {
        "id": 2,
        "goods_id": 2,
        "auction_title": "活动——2",
        "auction_content": "活动——2",
        "auction_scale": "0.02",
        "auction_price": "200.00000000",
        "auction_stock": 1,
        "auction_count": 0,
        "candy_cat_id": 1,
        "start_time": "2018-05-03 15:07:51",
        "end_time": "2018-05-08 15:07:49",
        "created_at": "2018-05-03 15:07:50",
        "updated_at": "2018-05-05 14:47:16",
        "picture": 4,
        "maxPrice": "130.00000000",
        "status": 3,
        "time_line": -1
    },
    {
        "id": 3,
        "goods_id": 3,
        "auction_title": "活动——3",
        "auction_content": "活动——3",
        "auction_scale": "0.03",
        "auction_price": "150.00000000",
        "auction_stock": 1,
        "auction_count": 6,
        "candy_cat_id": 1,
        "start_time": "2018-05-03 15:07:51",
        "end_time": "2018-05-15 15:07:49",
        "created_at": "2018-05-03 15:07:50",
        "updated_at": "2018-05-07 17:41:19",
        "picture": 4,
        "maxPrice": "550.00000000",
        "status": 2,
        "time_line": 102413
    },
    {
        "id": 4,
        "goods_id": 4,
        "auction_title": "活动——4",
        "auction_content": "活动——4",
        "auction_scale": "0.03",
        "auction_price": "200.00000000",
        "auction_stock": 1,
        "auction_count": 6,
        "candy_cat_id": 1,
        "start_time": "2018-05-03 15:07:51",
        "end_time": "2018-05-15 15:07:49",
        "created_at": "2018-05-03 15:07:50",
        "updated_at": "2018-05-05 14:47:08",
        "picture": 4,
        "maxPrice": "520.00000000",
        "status": 2,
        "time_line": 102413
    },
    {
        "id": 5,
        "goods_id": 5,
        "auction_title": "活动——5",
        "auction_content": "活动——5",
        "auction_scale": "0.001",
        "auction_price": "180.00000000",
        "auction_stock": 1,
        "auction_count": 6,
        "candy_cat_id": 1,
        "start_time": "2018-05-03 15:07:51",
        "end_time": "2018-05-15 15:07:49",
        "created_at": "2018-05-03 15:07:51",
        "updated_at": "2018-05-05 14:47:11",
        "picture": 4,
        "maxPrice": "366.00000000",
        "status": 2,
        "time_line": 102413
    },
    {
        "id": 6,
        "goods_id": 6,
        "auction_title": "活动——6",
        "auction_content": "活动——6",
        "auction_scale": "0.003",
        "auction_price": "200.00000000",
        "auction_stock": 1,
        "auction_count": 0,
        "candy_cat_id": 1,
        "start_time": "2018-05-16 11:05:35",
        "end_time": "2018-05-31 11:05:40",
        "created_at": "2018-05-14 11:05:43",
        "updated_at": "2018-05-14 11:05:46",
        "picture": 4,
        "maxPrice": null,
        "status": 1,
        "time_line": -1
    }
]

```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|id         |int		|yes		   |记录ID  |
|goods_id   |int		|yes		   |商品ID  |
|auction_scale|string	|yes		   |比例  |
|auction_price|string	|yes		   |起拍价  |
|auction_stock|int		|yes		   |库存  |
|auction_count|int		|yes		   |竞拍次数  |
|start_time  |string	|yes		   |开始竞拍时间  |
|end_time   |string		|yes		   |结束时间  |
|auction_title|string	|yes		   |活动名称  |
|auction_content|string	|yes		   |活动说明  |
|picture    |string		|yes		   |商品图  |
|maxPrice    |string	|yes		   |当前出价最高价  |
|status     |int	    |yes		   |1:未开始 2:进行中 3:结束  |
|time_line    |int  	|yes		   |时间差（秒数）  |



## 竞拍商品详情

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| id   | int  | 竞拍商品ID|
| limit| int  | 一页显示多少个|
| offset | int  | maxSize |
```
GET /api/v2/auction/detail
```
### HTTP Status Code

200

## 返回体

```json5
{
    "id": 3,
    "goods_id": 3,
    "auction_title": "活动——3",
    "auction_content": "活动——3",
    "auction_scale": "0.03",
    "auction_price": "150.00000000",
    "auction_stock": 1,
    "auction_count": 6,
    "candy_cat_id": 1,
    "start_time": "2018-05-03 15:07:51",
    "end_time": "2018-05-15 15:07:49",
    "created_at": "2018-05-03 15:07:50",
    "updated_at": "2018-05-07 17:41:19",
    "picture": 5,
    "record": [
        {
            "username": "lining",
            "price": "550.00000000",
            "auction_time": "2018-05-07 17:41:19"
        },
        {
            "username": "lining",
            "price": "481.00130000",
            "auction_time": "2018-05-12 14:48:45"
        },
        {
            "username": "lining",
            "price": "108.00000000",
            "auction_time": "2018-05-07 17:20:09"
        },
        {
            "username": "lining",
            "price": "103.00000000",
            "auction_time": "2018-05-07 17:20:06"
        }
    ],
    "user_counts": 8,
    "maxPrice": "550.00000000",
    "time_line": 102443,
    "type": 1
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|detail     |array		|yes		   |  |
|id         |int		|yes		   |记录ID  |
|goods_id   |int		|yes		   |商品ID  |
|auction_scale|string	|yes		   |比例  |
|auction_price|string	|yes		   |起拍价  |
|auction_stock|int		|yes		   |库存  |
|auction_status|int	    |yes		   |状态  |
|auction_count|int		|yes		   |总竞拍次数  |
|start_time  |string	|yes		   |开始竞拍时间  |
|end_time    |string	|yes		   |结束时间  |
|auction_title|string	|yes		   |活动名称  |
|auction_content|string	|yes		   |活动说明  |
|picture     |string	|yes		   |商品图  |
|user_counts |int	|yes		       |个人竞拍次数  |
|maxPrice     |int	    |yes		   |当前最高价  |
|time_line    |int  	|yes		   |时间差（秒数）  |
|type        |int	    |yes		   |0:未开始 1:活动进行中 2:余额不足 3:结束 |
|record      |array		|yes		   |  |
|username    |string	|yes		   |竞拍者名称  |
|price       |string	|yes		   |竞拍价  |
|auction_time |string	|yes		   |竞拍时间  |


## 开始竞拍

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| id   | int  | 竞拍商品ID|
```
GET /api/v2/auction/bidders
```
### HTTP Status Code

200

## 返回体

```json5
{
  "maxPrice": "455.00000000",
  "candy": "1570.00000000",
  "scale": "0.01"
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|maxPrice  |int	    |yes		   |当前最高价  |
|candy     |int	    |yes		   |当前余额  |
|scale     |string	|yes		   |比例  |


## 提交竞拍

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| id   | int  | 竞拍商品ID|
| price| int  | 竞拍价|
```
POST /api/v2/auction/up_bidders
```
### HTTP Status Code

201

## 返回体

```json5
{
  "code": "1",
  "msg": "竞拍成功"
}
{
  "code": "0",
  "msg": "竞拍价不能小于当前竞拍价"
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|msg  |string	  |yes		   |返回提示  |

## 竞拍记录列表

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|

```
GET /api/v2/auction/lists
```
### HTTP Status Code

200

## 返回体

```json5
[
    {
        "id": 12,
        "price": "112.00000000",
        "auction_id": 2,
        "count": 2,
        "auction_title": "活动——2",
        "picture": 4,
        "end_time": "2018-05-08 15:07:49",
        "type": 0
    },
    {
        "id": 21,
        "price": "210.00000000",
        "auction_id": 1,
        "count": 3,
        "auction_title": "活动——1",
        "picture": 4,
        "end_time": "2018-05-03 18:01:10",
        "type": 0
    },
    {
        "id": 32,
        "price": "300.00000000",
        "auction_id": 4,
        "count": 6,
        "auction_title": "活动——4",
        "picture": 4,
        "end_time": "2018-05-15 15:07:49",
        "type": 2
    },
    {
        "id": 33,
        "price": "300.00000000",
        "auction_id": 5,
        "count": 2,
        "auction_title": "活动——5",
        "picture": 4,
        "end_time": "2018-05-15 15:07:49",
        "type": 2
    },
    {
        "id": 36,
        "price": "550.00000000",
        "auction_id": 3,
        "count": 8,
        "auction_title": "活动——3",
        "picture": 4,
        "end_time": "2018-05-15 15:07:49",
        "type": 2
    }
]
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|id        |int	   |yes		   |竞拍ID  |
|auction_id        |int	  |yes		   |竞拍商品ID  |
|price       |string	  |yes		   |竞拍价格  |
|auction_title   |string	  |yes		   |活动标题  |
|picture       |string	  |yes		   |商品图  |
|auction_count  |string	  |yes		   |竞拍次数  |
|type      |int	  |yes		   |0:未中拍 1:已中拍 2:竞拍中 3:已发货 4:已完成  |

## 进入竞拍订单

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| id   | int  | 竞拍ID|

```
GET /api/v2/auction/getAuctionOrder
```
### HTTP Status Code

200

## 返回体

```json5
{
    "user_id": 2,
    "auction_id": 3,
    "price": "550.00000000",
    "auction_time": "2018-05-07 17:41:19",
    "auction_title": "活动——3",
    "auction_content": "活动——3",
    "picture": 4,
    "area": {
        "address_id": 1,
        "address_username": "王大麻子",
        "phone": "18040363559",
        "address": "四川省成都市武侯区,环球中心E2-1508"
    }
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|auction_id  |int	  |yes		   |竞拍商品ID  |
|price  |string	  |yes		   |竞拍价格  |
|auction_time  |string	  |yes		   |竞拍时间  |
|auction_title  |string	  |yes		   |活动标题  |
|picture  |string	  |yes		   |商品图片  |
|area    |array	  |yes		   |地址 0:没有地址 |
|address_id  |int	  |yes		   |收货ID  |
|address_username  |string	  |yes		   |收货人  |
|phone  |int	  |yes		   |手机号  |
|address  |string	  |yes		   |收货地址  |


## 提交竞拍订单

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| auction_id   | int  | 竞拍商品ID|
| address_id   | int  | 收货地址ID|

```
POST /api/v2/auction/upAuctionOrder
```
### HTTP Status Code

201

## 返回体

```json5
{
  "code": "1",
  "msg": "订单提交成功！"
}
{
  "code": "0",
  "msg": "收货地址不能为空！"
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|msg  |string	  |yes		   |返回信息  |


## 兑换商城首页

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| limit   | int  | 每页显示行数|
| offset   | int  | maxSize|

```
GET /api/v2/exchange/index
```

### HTTP Status Code

200

## 返回体

```json5
{
  "code": "1",
  "data": [
    {
      "id": 1,
      "goods_id": 1,
      "exchange_stock": 1,
      "exchange_price": "2000.00000000",
      "end_time": "2018-04-28 17:55:58",
      "created_at": "2018-05-07 14:59:52",
      "exchange_title": "测试——1",
      "picture": "asdasd"
    },
    {
      "id": 2,
      "goods_id": 1,
      "exchange_stock": 1,
      "exchange_price": "2050.00000000",
      "end_time": "2018-04-28 17:55:58",
      "created_at": "2018-05-07 14:59:52",
      "exchange_title": "测试——2",
      "picture": "asdasd"
    }
  ]
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|id  |int	  |yes		   |兑换商品ID  |
|goods_id  |int	  |yes		   |商品ID  |
|exchange_stock  |string	  |yes		   |兑换商品库存  |
|exchange_price  |string	  |yes		   |兑换商品价格  |
|end_time  |string	  |yes		   |结束时间  |
|exchange_title  |string	  |yes		   |活动标题  |
|picture  |string	  |yes		   |商品图片  |


## 兑换商城详情

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| id   | int  | 兑换商品ID|

```
GET /api/v2/exchange/detail
```
### HTTP Status Code

200

## 返回体

```json5
{
  "code": "1",
  "detail": {
    "id": 1,
    "goods_id": 1,
    "exchange_stock": 1,
    "exchange_price": "2000.00000000",
    "end_time": "2018-04-28 17:55:58",
    "created_at": "2018-05-07 14:59:52",
    "exchange_title": "测试——1",
    "exchange_content": "测试——content",
    "picture": "asdasd"
  }
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|id  |int	  |yes		   |兑换商品ID  |
|goods_id  |int	  |yes		   |商品ID  |
|exchange_stock  |string	  |yes		   |兑换商品库存  |
|exchange_price  |string	  |yes		   |兑换商品价格  |
|end_time  |string	  |yes		   |结束时间  |
|exchange_title  |string	  |yes		   |活动标题  |
|exchange_content  |string	  |yes		   |活动说明  |
|picture  |string	  |yes		   |商品图片  |


## 确认兑换订单

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| id   | int  | 兑换商品ID|

```
GET /api/v2/exchange/getExchangeOrder
```
### HTTP Status Code

200

## 返回体

```json5

{
  "code": "0",
  "msg": "余额不足！"
}

{
  "code": 1,
  "exchange": [
    {
      "exchange_id": 1,
      "exchange_price": "2000.00000000",
      "exchange_stock": 1,
      "exchange_title": "测试——1",
      "picture": "asdasd"
    }
  ],
  "address": {
    "address_id": 1,
    "address_username": "张三",
    "phone": "18040363559",
    "address": "威武霸气大中国"
  }
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|exchange  |array	  |yes		   |订单详情  |
|exchange_id  |int	  |yes		   |兑换商品ID  |
|exchange_price  |string	  |yes		   |兑换价格  |
|exchange_stock  |string	  |yes		   |库存  |
|exchange_title  |string	  |yes		   |活动标题  |
|picture  |string	  |yes		   |商品图片  |
|address  |string	  |yes		   |array |
|address_id  |int	  |yes		   |收货ID  |
|address_username  |string	  |yes		   |收货人  |
|phone  |int	  |yes		   |手机号  |
|address  |string	  |yes		   |收货地址  |

## 提交竞拍订单

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| exchange_id  | int  | 兑换商品ID|
| address_id   | int  | 收货地址ID|

```
POST /api/v2/exchange/getAuctionOrder
```
### HTTP Status Code

201

## 返回体

```json5
{
  "code": "1",
  "msg": "订单提交成功！"
}
{
  "code": "0",
  "msg": "收货地址不能为空！"
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|msg  |string	  |yes		   |返回信息  |


## 兑换订单列表

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|


```
GET /api/v2/exchange/lists
```
### HTTP Status Code

200

## 返回体

```json5
[
  {
    "id": 1,
    "exchange_stock": 1,
    "exchange_price": "2000.00000000",
    "end_time": "2018-04-28 17:55:58",
    "created_at": "2018-05-07 14:59:52",
    "exchange_title": "测试——1",
    "picture": "asdasd"
  }，
  {
      "id": 2,
      "exchange_stock": 1,
      "exchange_price": "2000.00000000",
      "end_time": "2018-04-28 17:55:58",
      "created_at": "2018-05-07 14:59:52",
      "exchange_title": "测试——1",
      "picture": "asdasd"
    }
]
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|id  |string	  |yes		   |兑换商品id  |
|exchange_stock  |string	  |yes		   |库存  |
|exchange_price  |string	  |yes		   |兑换价格  |
|end_time  |string	  |yes		   |结束时间  |
|exchange_title  |string	  |yes		   |活动标题  |
|picture  |string	  |yes		   |图片  |



## 收货地址列表

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|


```
GET /api/v2/address/lists
```
### HTTP Status Code

200

## 返回体

```json5
[
  {
    "id": 1,
    "user_id": 2,
    "username": "张三",
    "phone": "18040363559",
    "status": 1,
    "address": "威武霸气大中国",
    "created_at": "2018-05-04 11:33:22",
    "updated_at": "2018-05-04 11:33:22"
  },
  {
      "id": 2,
      "user_id": 2,
      "username": "张三",
      "phone": "18040363559",
      "status": 0,
      "address": "威武霸气大中国",
      "created_at": "2018-05-04 11:33:22",
      "updated_at": "2018-05-04 11:33:22"
    },
  {
      "id": 3,
      "user_id": 3,
      "username": "李四",
      "phone": "18040363559",
      "status": 1,
      "address": "威武霸气大中国",
      "created_at": "2018-05-04 11:33:22",
      "updated_at": "2018-05-04 11:33:22"
    },
   {
       "id": 4,
       "user_id": 3,
       "username": "李四",
       "phone": "18040363559",
       "status": 0,
       "address": "威武霸气大中国",
       "created_at": "2018-05-04 11:33:22",
       "updated_at": "2018-05-04 11:33:22"
     }
]
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|id  |int	  |yes		   |地址ID  |
|user_id  |int	  |yes		   |用户ID  |
|username  |string	  |yes		   |收货人  |
|phone  |int	  |yes		   |手机号  |
|status  |int	  |yes		   |1：默认地址 0：其他地址  |
|address  |string	  |yes		   |详细地址  |


## 查看收货地址详情

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| id  | int  | 收货地址ID|


```
GET /api/v2/address/show/{id}
```
### HTTP Status Code

200

## 返回体

```json5
{
  "id": 1,
  "user_id": 2,
  "username": "张三",
  "phone": "18040363559",
  "status": 1,
  "address": "威武霸气大中国",
  "created_at": "2018-05-04 11:33:22",
  "updated_at": "2018-05-04 11:33:22"
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|id  |int	  |yes		   |地址ID  |
|user_id  |int	  |yes		   |用户ID  |
|username  |string	  |yes		   |收货人  |
|phone  |int	  |yes		   |手机号  |
|status  |int	  |yes		   |1：默认地址 0：其他地址  |
|address  |string	  |yes		   |详细地址  |


## 编辑收货地址

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| id  | int  | 收货地址ID|
| username  | String  | 收货人姓名|
| phone  | int  | 手机号|
| address  | String  | 详细地址|


```
POST /api/v2/address/edit
```
### HTTP Status Code

201

## 返回体

```json5
{
  'code':'1',
  'msg' : '修改成功'
}

{
  "message": "提交的信息验证错误",
  "errors": {
    "phone": [
      "手机号不能超过11位"
    ]
  }
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|msg  |string	  |yes		   |返回信息  |


## 添加收货地址

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| username  | String  | 收货人姓名|
| phone  | int  | 手机号|
| address  | String  | 详细地址|


```
POST /api/v2/address/add
```
### HTTP Status Code

201

## 返回体

```json5
{
  'code':'1',
  'msg' : '修改成功'
}

{
  "message": "提交的信息验证错误",
  "errors": {
    "phone": [
      "手机号不能超过11位"
    ]
  }
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|msg  |string	  |yes		   |返回信息  |

## 修改默认收货地址

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| id  | int  | 收货地址ID|

```
POST /api/v2/address/updateStatus
```
### HTTP Status Code

201

## 返回体

```json5
{
  'code':'1',
  'msg' : '修改成功'
}

```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|msg  |string	  |yes		   |返回信息  |


## 删除收货地址

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| id  | int  | 收货地址ID|

```
POST /api/v2/address/delete
```
### HTTP Status Code

204

## 返回体

```json5
{
  'code':'1',
  'msg' : '删除成功'
}

```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|msg  |string	  |yes		   |返回信息  |


##  省市区三级联动

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| id  | int  | id|

```
POST /api/v2/getArea
```
### HTTP Status Code

200

## 返回体




