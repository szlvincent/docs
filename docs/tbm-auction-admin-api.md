# 积分商城API

## 竞拍商品

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| limit   | int  | 一页显示多少个|
| page | int | 页码 |
| keyword | string | 搜索字 |
| status | int | 状态:1-售完 2-库存中 3-出售中|

```
GET /tbm-goods/goods/lists
```
### HTTP Status Code

200

## 返回体

```json5
[{
	"id": 1,
	"title": "测试——1",
	"content": "测试——content",
	"stock": 7,
	"status": 2,
	"picture": "asdasd",
	"created_at": "2018-05-05 11:58:32",
	"updated_at": "2018-04-28 11:24:50"
}, {
	"id": 2,
	"title": "测试——2",
	"content": "测试——content",
	"stock": 6,
	"status": 2,
	"picture": "asdasd",
	"created_at": "2018-05-05 11:58:33",
	"updated_at": "2018-04-28 11:25:16"
}, {
	"id": 3,
	"title": "测试——3",
	"content": "测试——content",
	"stock": 2,
	"status": 2,
	"picture": "asdasd",
	"created_at": "2018-05-08 15:30:30",
	"updated_at": "2018-04-28 11:25:18"
}, {
	"id": 4,
	"title": "测试——4",
	"content": "测试——content",
	"stock": 10,
	"status": 1,
	"picture": "asdasd",
	"created_at": "2018-05-05 11:58:33",
	"updated_at": "2018-04-28 11:25:17"
}, {
	"id": 5,
	"title": "测试——5",
	"content": "测试——content",
	"stock": 10,
	"status": 1,
	"picture": "asdasd",
	"created_at": "2018-05-05 11:58:34",
	"updated_at": "2018-04-28 11:25:16"
}]
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|id         |int		|yes		   |商品ID  |
|title      |string		|yes		   |商品名称  |
|content    |string		|yes		   |商品介绍  |
|stock      |int		|yes		   |库存  |
|status     |int	    |yes		   |状态  |
|picture    |string		|yes		   |商品图  |
|updated_at |string		|yes		   |创建时间  |
|updated_at |string		|yes		   |更新时间  |

## 进入编辑商品

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| id   | int  | 商品ID|

```
GET /tbm-goods/goods/show/{goods}
```
### HTTP Status Code

200

## 返回体

```json5
{
	"id": 3,
	"title": "测试——3",
	"content": "测试——content",
	"stock": 0,
	"status": 2,
	"picture": "asdasd",
	"updated_at": "2018-05-05 11:58:51",
	"created_at": "2018-04-28 11:25:18"
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|id         |int		|yes		   |记录ID  |
|goods_id   |int		|yes		   |商品ID  |
|auction_scale|string		|yes		   |比例  |
|auction_price|string	|yes		   |起拍价  |
|auction_stock|int		|yes		   |库存  |
|auction_status|int	|yes		   |状态  |
|auction_count|int		|yes		   |竞拍次数  |
|start_time  |string		|yes		   |开始竞拍时间  |
|end_time   |string		|yes		   |结束时间  |
|title      |string		|yes		   |商品名称  |
|picture    |string		|yes		   |商品图  |


## 提交编辑商品

### 参数

| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| id   | int  | 商品ID|
| type | int  | 类型 |
| title| string  | 商品标题|
| content | string  | 商品介绍 |
| stock | int  | 库存 |
| picture | string  | 图片ID |

```
POST /tbm-goods/goods/edit_goods
```
### HTTP Status Code

200

## 返回体

```json5
{
  "code": "1",
  "msg": "修改成功"
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|msg     |array		|yes		   |返回信息  |

## 添加商品

### 参数

| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| type | int  | 类型 |
| title| string  | 商品标题|
| content | string  | 商品介绍 |
| stock | int  | 库存 |
| picture | string  | 图片ID |

```
POST /tbm-goods/goods/add_goods
```
### HTTP Status Code

201

## 返回体

```json5
{
  "code": "1",
  "msg": "修改成功"
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|msg     |array		|yes		   |返回信息  |


## 删除商品

### 参数

| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| id   | int  | 商品ID|

```
POST /tbm-goods/goods/deleted
```
### HTTP Status Code

204

## 返回体

```json5
{
  "code": "1",
  "msg": "删除成功"
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|msg     |array		|yes		   |返回信息  |


## 竞拍列表

### 参数

| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| limit   | int  | 分页|
| page | int | 页码 |
| keyword | string | 搜索字 |
| status | int | 1:流拍 2:竞拍结束 3:拍卖中 |

```
GET /tbm-goods/goods/auction/lists
```
### HTTP Status Code

200

## 返回体

```json5
{
	"current_page": 1,
	"data": [{
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
		"picture": "{\"goodsImgId\":4,\"detailImgId\":5}",
		"type": 1,
		"title": "测试——1",
		"content": "测试——content",
		"maxPrice": "455.00000000"
	}, {
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
		"picture": "{\"goodsImgId\":4,\"detailImgId\":5}",
		"type": 1,
		"title": "测试——2",
		"content": "测试——content",
		"maxPrice": "130.00000000"
	}, {
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
		"picture": "{\"goodsImgId\":4,\"detailImgId\":5}",
		"type": 1,
		"title": "测试——3",
		"content": "测试——content",
		"maxPrice": "550.00000000"
	}, {
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
		"picture": "{\"goodsImgId\":4,\"detailImgId\":5}",
		"type": 1,
		"title": "测试——4",
		"content": "测试——content",
		"maxPrice": "520.00000000"
	}, {
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
		"picture": "{\"goodsImgId\":4,\"detailImgId\":5}",
		"type": 1,
		"title": "测试——5",
		"content": "测试——content",
		"maxPrice": "366.00000000"
	}],
	"first_page_url": "http:\/\/www.token.com\/tbm-goods\/goods\/auction\/lists?page=1",
	"from": 1,
	"last_page": 1,
	"last_page_url": "http:\/\/www.token.com\/tbm-goods\/goods\/auction\/lists?page=1",
	"next_page_url": null,
	"path": "http:\/\/www.token.com\/tbm-goods\/goods\/auction\/lists",
	"per_page": 10,
	"prev_page_url": null,
	"to": 5,
	"total": 5
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|id         |int		|yes		   |竞拍商品ID  |
|goods_id   |int		|yes		   |商品ID  |
|auction_title|string	|yes		   |活动名称  |
|auction_content|string	|yes		   |活动说明  |
|auction_scale|int		|yes		   |比例  |
|auction_price|string	|yes		   |起拍价  |
|auction_stock|int		|yes		   |库存  |
|auction_count|int		|yes		   |总竞拍次数  |
|start_time  |string	|yes		   |开始竞拍时间  |
|end_time    |string	|yes		   |结束时间  |
|title       |string	|yes		   |商品名称  |
|type        |int	    |yes		   |商品类型:1-实物 2-虚拟  |
|title       |string	|yes		   |商品名称  |
|content     |string	|yes		   |商品结束  |
|maxPrice     |string	|yes		   |成交价  |

## 添加竞拍

### 参数

| 名称 | 类型 | 描述 |
|:----:|:----:|------|
|goods_id       |int				|商品ID  |
|auction_title  |string				|活动名称  |
|auction_content  |string				|活动说明  |
|auction_scale  |int				|比例  |
|auction_price  |string			    |起拍价  |
|auction_stock  |int			   |库存  |
|candy_cat_id   |int			   |钱包分类ID  |
|start_time     |string			|开始竞拍时间  |
|end_time       |string			 |结束时间  |
```
POST /tbm-goods/goods/auction/add_auction
```
### HTTP Status Code

200

## 返回体

```json5
{
  "code": "1",
  "msg": "添加成功"
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|msg         |string		|yes		   |返回信息  |


## 进入编辑竞拍

### 参数

| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| id   | int  | 竞拍商品ID|

```
GET /tbm-goods/goods/auction/show
```
### HTTP Status Code

200

## 返回体

```json5
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
	"title": "测试——1",
	"picture": "asdasd"
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|id         |int		|yes		   |竞拍商品ID  |
|goods_id   |int		|yes		   |商品ID  |
|auction_title  |string	 |yes			|活动名称  |
|auction_content  |string	|yes			|活动说明  |
|auction_scale|int		|yes		   |比例  |
|auction_price|string	|yes		   |起拍价  |
|auction_stock|int		|yes		   |库存  |
|auction_status|int	    |yes		   |状态  |
|auction_count|int		|yes		   |总竞拍次数  |
|start_time  |string	|yes		   |开始竞拍时间  |
|end_time    |string	|yes		   |结束时间  |
|title       |string	|yes		   |商品名称  |
|picture     |string	|yes		   |商品图  |


## 提交编辑竞拍

### 参数

| 名称 | 类型 | 描述 |
|:----:|:----:|------|
|id             |int				|竞拍商品ID  |
|goods_id       |int				|商品ID  |
|auction_title  |string				|活动名称  |
|auction_content  |string			|活动说明  |
|auction_scale  |int				|比例  |
|auction_price  |string			    |起拍价  |
|auction_stock  |int			   |库存  |
|candy_cat_id   |int			   |钱包分类ID  |
|start_time     |string			    |开始竞拍时间  |
|end_time       |string			    |结束时间  |
```
POST /tbm-goods/goods/auction/edit_auction
```
### HTTP Status Code

201

## 返回体

```json5
{
  "code": "1",
  "msg": "修改成功"
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|msg         |string		|yes		   |返回信息  |



## 删除竞拍商品

### 参数

| 名称 | 类型 | 描述 |
|:----:|:----:|------|
|id             |int				|竞拍商品ID  |

```
POST /tbm-goods/goods/auction/deleted/{id}
```
### HTTP Status Code

204

## 返回体

```json5
{
  "code": "1",
  "msg": "删除成功"
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|msg         |string		|yes		   |返回信息  |

## 竞拍记录列表

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| limit  | string  | 行数|
| page | int | 页码 |
| filed  | string  | 查询字段:auction_title、username|
| keyword  | string  | 搜索字|
| auction_id  | int  | 竞拍商品ID|

```
GET /tbm-goods/goods/auction/auction_lists
```
### HTTP Status Code

200

## 返回体

```json5
{
	"current_page": 1,
	"data": [{
		"id": 1,
		"username": "lining",
		"price": "101.00000000",
		"auction_time": "2018-05-07 17:20:05",
		"count": 1,
		"auction_id": 1,
		"auction_title": "活动——1",
		"picture": "asdasd"
	}, {
		"id": 2,
		"username": "lining",
		"price": "102.00000000",
		"auction_time": "2018-05-07 17:20:05",
		"count": 1,
		"auction_id": 2,
		"auction_title": "活动——2",
		"picture": "asdasd"
	}, {
		"id": 3,
		"username": "lining",
		"price": "103.00000000",
		"auction_time": "2018-05-07 17:20:06",
		"count": 1,
		"auction_id": 3,
		"auction_title": "活动——3",
		"picture": "asdasd"
	}, {
		"id": 4,
		"username": "lining",
		"price": "104.00000000",
		"auction_time": "2018-05-07 17:20:08",
		"count": 1,
		"auction_id": 4,
		"auction_title": "活动——4",
		"picture": "asdasd"
	}, {
		"id": 5,
		"username": "lining",
		"price": "105.00000000",
		"auction_time": "2018-05-07 17:20:08",
		"count": 1,
		"auction_id": 5,
		"auction_title": "活动——5",
		"picture": "asdasd"
	}, {
		"id": 6,
		"username": "lining",
		"price": "106.00000000",
		"auction_time": "2018-05-07 17:20:08",
		"count": 1,
		"auction_id": 1,
		"auction_title": "活动——1",
		"picture": "asdasd"
	}, {
		"id": 7,
		"username": "lining",
		"price": "107.00000000",
		"auction_time": "2018-05-07 17:20:09",
		"count": 1,
		"auction_id": 2,
		"auction_title": "活动——2",
		"picture": "asdasd"
	}, {
		"id": 8,
		"username": "lining",
		"price": "108.00000000",
		"auction_time": "2018-05-07 17:20:09",
		"count": 1,
		"auction_id": 3,
		"auction_title": "活动——3",
		"picture": "asdasd"
	}, {
		"id": 9,
		"username": "lining",
		"price": "109.00000000",
		"auction_time": "2018-05-07 17:20:11",
		"count": 1,
		"auction_id": 4,
		"auction_title": "活动——4",
		"picture": "asdasd"
	}, {
		"id": 10,
		"username": "lining",
		"price": "110.00000000",
		"auction_time": "2018-05-07 17:20:11",
		"count": 1,
		"auction_id": 5,
		"auction_title": "活动——5",
		"picture": "asdasd"
	}],
	"first_page_url": "http:\/\/www.token.com\/tbm-goods\/goods\/auction\/auction_lists?page=1",
	"from": 1,
	"last_page": 2,
	"last_page_url": "http:\/\/www.token.com\/tbm-goods\/goods\/auction\/auction_lists?page=2",
	"next_page_url": "http:\/\/www.token.com\/tbm-goods\/goods\/auction\/auction_lists?page=2",
	"path": "http:\/\/www.token.com\/tbm-goods\/goods\/auction\/auction_lists",
	"per_page": 10,
	"prev_page_url": null,
	"to": 10,
	"total": 20
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|username  |string	  |yes		   |用户名  |
|price  |string	  |yes		   |竞拍价  |
|auction_time  |string	  |yes		   |竞拍时间  |
|count  |string	  |yes		   |竞拍次数  |
|auction_id  |string	  |yes		   |竞拍商品ID  |
|auction_title  |string	  |yes		   |活动标题  |
|picture  |string	  |yes		   |商品图片  |
|current_page  |string	  |yes		   |当前页  |
|last_page  |string	  |yes		   |下一页  |
|per_page  |string	  |yes		   |每页显示数量  |
|picture  |string	  |yes		   |商品图片  |
|total  |string	  |yes		   |总数量  |


## 竞拍成功列表

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| limit  | string  | 页码|
| filed  | string  | 查询字段|
| keyword  | string  | 搜索字|

```
GET /tbm-goods/goods/auction/auction_success
```
### HTTP Status Code

200

## 返回体

```json5
[{
	"auction_id": 1,
	"user_id": 5,
	"price": "455.00000000",
	"username": "lining",
	"auction_time": "2018-05-07 17:20:14",
	"auction_title": "活动——1",
	"picture": "asdasd",
	"address": null,
	"phone": null,
	"nickname": null
}, {
	"auction_id": 2,
	"user_id": 3,
	"price": "130.00000000",
	"username": "lining",
	"auction_time": "2018-05-07 17:20:13",
	"auction_title": "活动——2",
	"picture": "asdasd",
	"address": "四川省成都市简阳市,不知道怎么办啊",
	"phone": "18200394531",
	"nickname": "卿大侠"
}]
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|username  |string	  |yes		   |用户名  |
|price  |string	  |yes		   |竞拍价  |
|auction_time  |string	  |yes		   |竞拍时间  |
|count  |string	  |yes		   |竞拍次数  |
|auction_id  |string	  |yes		   |竞拍商品ID  |
|auction_title  |string	  |yes		   |活动标题  |
|picture  |string	  |yes		   |商品图片  |
|current_page  |string	  |yes		   |当前页  |
|last_page  |string	  |yes		   |下一页  |
|per_page  |string	  |yes		   |每页显示数量  |
|picture  |string	  |yes		   |商品图片  |
|total  |string	  |yes		   |总数量  |


## 兑换商品列表

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| limit  | int  | 行数|
| page  | int  | 页码|
| status  | int  | 1:兑换中 2:兑换结束  3:售完|
| keyword  | string  | 搜索字|

```
GET /tbm-goods/goods/exchange
```
### HTTP Status Code

200

## 返回体

```json5
{
	"current_page": 1,
	"data": [{
		"id": 1,
		"goods_id": 1,
		"exchange_price": "2000.00000000",
		"exchange_stock": 1,
		"candy_cat_id": 1,
		"end_time": "2018-05-15 17:55:58",
		"created_at": "2018-04-28 17:55:58",
		"updated_at": "2018-05-07 14:59:52",
		"exchange_title": "活动——1",
		"exchange_content": "活动——1",
		"picture": "asdasd"
	}, {
		"id": 2,
		"goods_id": 10,
		"exchange_price": "350.00000000",
		"exchange_stock": 10,
		"candy_cat_id": 1,
		"end_time": "2018-05-15 15:07:49",
		"created_at": "2018-05-11 03:09:32",
		"updated_at": "2018-05-11 03:09:32",
		"exchange_title": "活动——2",
		"exchange_content": "活动——2",
		"picture": "{img1:1,img2:2}"
	}],
	"first_page_url": "http:\/\/www.token.com\/tbm-goods\/goods\/exchange?page=1",
	"from": 1,
	"last_page": 1,
	"last_page_url": "http:\/\/www.token.com\/tbm-goods\/goods\/exchange?page=1",
	"next_page_url": null,
	"path": "http:\/\/www.token.com\/tbm-goods\/goods\/exchange",
	"per_page": 10,
	"prev_page_url": null,
	"to": 2,
	"total": 2
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|id  |int	  |yes		   |兑换商品ID  |
|goods_id  |int	  |yes		   |商品ID  |
|exchange_price  |int	  |yes		   |兑换价  |
|exchange_stock  |string	  |yes		   |兑换库存  |
|end_time  |string	  |yes		   |结束时间  |
|exchange_title  |string	  |yes		   |活动标题  |
|exchange_content  |string	  |yes		   |活动说明  |
|picture  |json	  |yes		   |商品图片ID  |


## 添加兑换商品

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| goods_id  | int  | 商品ID|
| exchange_title  |string	   |活动标题  |
| exchange_content  |string	   |活动说明  |
| exchange_stock  | int  | 库存|
| exchange_price  | int  | 兑换价|
| candy_cat_id  | int  | 钱包分类ID|
| end_time  | string  | 结束时间|


```
GET /tbm-goods/goods/exchange/add_exchange
```
### HTTP Status Code

201

## 返回体

```json5
{
	"code": 1,
	"msg": "添加成功"
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|msg  |string	  |yes		   |返回结果  |



## 查看兑换商品详情

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| id  | int  | 兑换商品ID|

```
GET /tbm-goods/goods/exchange/show
```
### HTTP Status Code

200

## 返回体

```json5
{
	"id": 1,
	"goods_id": 1,
	"exchange_price": "2000.00000000",
	"candy_cat_id": 1,
	"exchange_stock": 1,
	"end_time": "2018-05-15 17:55:58",
	"exchange_title": "活动——1",
	"exchange_content": "活动——1",
	"picture": "asdasd"
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|id  |int	  |yes		   |兑换商品ID  |
|goods_id  |int	  |yes		   |商品ID  |
|exchange_price  |int	  |yes		   |兑换价格  |
|candy_cat_id  |int	  |yes		   |钱包分类ID  |
|exchange_stock  |int	  |yes		   |库存  |
|end_time  |string	  |yes		   |结束时间  |
|exchange_title  |string	  |yes		   |活动标题  |
|exchange_content  |string	  |yes		   |活动说明  |
|picture  |string	  |yes		   |图片  |



## 修改兑换商品

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| id  | int  | 兑换商品ID|
| goods_id  | int  | 商品ID|
| exchange_title  |string	   |活动标题  |
| exchange_content  |string	   |活动说明  |
| exchange_stock  | int  | 库存|
| exchange_price  | int  | 兑换价|
| candy_cat_id  | int  | 钱包分类ID|
| end_time  | string  | 结束时间|
```
POST /tbm-goods/goods/exchange/edit_exchange
```
### HTTP Status Code

201

## 返回体

```json5
{
	"code": 1,
	"msg": "修改成功"
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|msg  |string	  |yes		   |返回结果  |


## 删除兑换商品

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| id  | int  | 兑换商品ID|

```
POST /tbm-goods/goods/exchange/deleted/{id}
```
### HTTP Status Code

204

## 返回体

```json5
{
	"code": 1,
	"msg": "删除成功"
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|msg  |string	  |yes		   |返回结果  |


## 兑换记录列表

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| limit  | int  | 分页|
| keyword  | string  | 搜索字|
```
GET /tbm-goods/goods/exchange/lists
```
### HTTP Status Code

200

## 返回体

```json5
{
	"current_page": 1,
	"data": [{
		"order_id": "2018050707240452995355",
		"deliver": 1,
		"remark": null,
		"exchange_title": "测试——1",
		"picture": "asdasd",
		"exchange_price": "2000.00000000",
		"username": "王大麻子",
		"phone": "18040363559",
		"address": "四川省成都市武侯区,环球中心E2-1508"
	}],
	"first_page_url": "http:\/\/www.token.com\/tbm-goods\/goods\/exchange\/lists?page=1",
	"from": 1,
	"last_page": 1,
	"last_page_url": "http:\/\/www.token.com\/tbm-goods\/goods\/exchange\/lists?page=1",
	"next_page_url": null,
	"path": "http:\/\/www.token.com\/tbm-goods\/goods\/exchange\/lists",
	"per_page": 10,
	"prev_page_url": null,
	"to": 1,
	"total": 1
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
|order_id  |int	  |yes		   |订单ID  |
|deliver  |int	  |yes		   |1:发货  2:未发货  |
|remark  |string	  |yes		   |备注  |
|exchange_title  |string	  |yes		   |活动标题  |
|picture  |json	  |yes		   |商品图  |
|exchange_price  |string	  |yes		   |兑换价格  |
|username  |string	  |yes		   |收货人  |
|phone  |string	  |yes		   |手机号  |
|address  |string	  |yes		   |详细地址  |


## 点击发货

### 参数
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| id  | int  | 订单ID|
```
POST /tbm-goods/goods/collectGoods/{id}
```
### HTTP Status Code

201

## 返回体

```json5
{
  "code":1
}
```
## 返回字段

| name     | type     | must     | description |
|----------|:--------:|:--------:|:--------:|
