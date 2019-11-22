# 小程序项目API文档

# 首页

## 轮播图

### 基本信息

- Path： http://www.tpthink.cn/api/v1/banner/1
- Method：GET
- 接口描述：

### 请求参数

- 路径参数

### 返回数据

- 操作成功响应状态码：200

| 名称          | 类型     | 是否必须 | 默认值                | 备注       |
| ------------- | -------- | -------- | --------------------- | ---------- |
| id            | int      | 是       |                       | ID         |
| name          | String   | 是       |                       | 轮播图名称 |
| description   | String   | 是       |                       | 描述       |
| update_time   | String   | 是       | "1970-01-01 08:00:00" | 更新时间   |
| items         | object[] | 是       |                       |            |
| ├─key_word    | string   | 是       |                       |            |
| ├─type        | int      | 是       |                       |            |
| ├─update_time | String   | 是       |                       | 更新时间   |
| ├─img         | object   |          |                       |            |
| ├─url         | String   | 是       |                       | 图片路径   |
| ├─update_time | String   |          |                       | 更新时间   |

```json
{
    "id": 1,
    "name": "首页置顶",
    "description": "首页轮播图",
    "update_time": "1970-01-01 08:00:00",
    "items": [
        {
            "key_word": "6",
            "type": 1,
            "update_time": "1970-01-01 08:00:00",
            "img": {
                "url": "http://www.tpthink.cn/images/banner-4a.png",
                "update_time": "1970-01-01 08:00:00"
            }
        },
        {
            "key_word": "25",
            "type": 1,
            "update_time": "1970-01-01 08:00:00",
            "img": {
                "url": "http://www.tpthink.cn/images/banner-2a.png",
                "update_time": "1970-01-01 08:00:00"
            }
        }
    ]
}
```



## 专题栏位

### 基本信息

- Path：  http://www.tpthink.cn/api/v1/theme?ids=1,2,3
- Method：GET
- 接口描述：

### 请求参数

- 查询参数：ids为专栏id，多个用逗号分隔

### 返回数据

- 操作成功响应状态码：200

| 名称          | 类型      | 是否必须 | 默认值                | 备注     |
| ------------- | --------- | -------- | --------------------- | -------- |
|               | object [] | 是       |                       |          |
| ├─id          | String    | 是       | "1970-01-01 08:00:00" | 更新时间 |
| ├─name        | object[]  | 是       |                       |          |
| ├─description | string    | 是       |                       |          |
| ├─update_time | String    | 是       |                       | 更新时间 |
| ├─topic_img   | object    |          |                       |          |
| ├─url         | String    | 是       |                       | 图片路径 |
| ├─update_time | String    |          |                       | 更新时间 |
| ├─head_img    |           |          |                       |          |
| ├─url         |           |          |                       |          |
| ├─update_time |           |          |                       |          |

```json
[
    {
        "id": 1,
        "name": "专题栏位一",
        "description": "美味水果世界",
        "update_time": "1970-01-01 08:00:00",
        "topic_img": {
            "url": "http://www.tpthink.cn/images/1@theme.png",
            "update_time": "1970-01-01 08:00:00"
        },
        "head_img": {
            "url": "http://www.tpthink.cn/images/1@theme-head.png",
            "update_time": "1970-01-01 08:00:00"
        }
    },
    {
        "id": 2,
        "name": "专题栏位二",
        "description": "新品推荐",
        "update_time": "1970-01-01 08:00:00",
        "topic_img": {
            "url": "http://www.tpthink.cn/images/2@theme.png",
            "update_time": "1970-01-01 08:00:00"
        },
        "head_img": {
            "url": "http://www.tpthink.cn/images/2@theme-head.png",
            "update_time": "1970-01-01 08:00:00"
        }
    }
]
```



## 最近新品

### 基本信息

- Path：   http://www.tpthink.cn/api/v1/product/recent
- Method：GET
- 接口描述：

### 请求参数

- 查询参数ids

### 返回数据

- 操作成功响应状态码：200

```json
[
    {
        "id": 1,
        "name": "芹菜 半斤",
        "price": "0.01",
        "stock": 998,
        "main_img_url": "http://www.tpthink.cn/images/product-vg@1.png",
        "img_id": 13
    },
    {
        "id": 2,
        "name": "梨花带雨 3个",
        "price": "0.01",
        "stock": 984,
        "main_img_url": "http://www.tpthink.cn/images/product-dryfruit@1.png",
        "img_id": 10
    }
]
```



# 商品

## 获取商品分类

### 基本信息

- Path： http://www.tpthink.cn/api/v1/category/all
- Method：GET
- 接口描述：

### 请求参数

### 返回数据

- 操作成功响应状态码：200

```json
[
    {
        "id": 2,
        "name": "果味",
        "topic_img_id": 6,
        "description": null,
        "update_time": "1970-01-01 08:00:00",
        "img": {
            "url": "http://www.tpthink.cn/images/category-dryfruit.png",
            "update_time": "1970-01-01 08:00:00"
        }
    },
    {
        "id": 3,
        "name": "蔬菜",
        "topic_img_id": 5,
        "description": null,
        "update_time": "1970-01-01 08:00:00",
        "img": {
            "url": "http://www.tpthink.cn/images/category-vg.png",
            "update_time": "1970-01-01 08:00:00"
        }
    }
]
```



## 获取商品分类下的商品

### 基本信息

- Path：  http://www.tpthink.cn/api/v1/product/by_category?id=2
- Method：GET
- 接口描述：

### 请求参数

- 查询参数：id为商品分类id

### 返回数据

- 操作成功响应状态码：200

```json
[
    {
        "id": 2,
        "name": "梨花带雨 3个",
        "price": "0.01",
        "stock": 984,
        "main_img_url": "http://www.tpthink.cn/images/product-dryfruit@1.png",
        "img_id": 10
    },
    {
        "id": 5,
        "name": "春生龙眼 500克",
        "price": "0.01",
        "stock": 995,
        "main_img_url": "http://www.tpthink.cn/images/product-dryfruit@2.png",
        "img_id": 33
    }
]
```



## 获取商品信息

### 基本信息

- Path：   http://www.tpthink.cn/api/v1/product/2
- Method：GET
- 接口描述：

### 请求参数

- 路径参数：数字为商品id

### 返回数据

- 操作成功响应状态码：200

```json
{
    "id": 2,
    "name": "梨花带雨 3个",
    "price": "0.01",
    "stock": 984,
    "main_img_url": "http://www.tpthink.cn/images/product-dryfruit@1.png",
    "summary": null,
    "img_id": 10,
    "imgs": [],
    "properties": [
        {
            "name": "品名",
            "detail": "梨子",
            "update_time": "1970-01-01 08:00:00"
        },
        {
            "name": "产地",
            "detail": "金星",
            "update_time": "1970-01-01 08:00:00"
        },
        {
            "name": "净含量",
            "detail": "100g",
            "update_time": "1970-01-01 08:00:00"
        },
        {
            "name": "保质期",
            "detail": "10天",
            "update_time": "1970-01-01 08:00:00"
        }
    ]
}
```





# 订单

## 获取用户订单列表

### 基本信息

- Path：  http://www.tpthink.cn/api/v1/order/by_user?page=1
- Method：GET
- 接口描述：

### 请求参数

- 查询参数：page为页面

### 返回数据

- 操作成功响应状态码：200

```json
{
    "current_page": 1,
    "data": [
        {
            "id": 46,
            "order_no": "CB15891253844855",
            "create_time": "2019-11-15 11:38:45",
            "total_price": "0.02",
            "status": 1,
            "snap_img": "http://www.tpthink.cn/images/product-dryfruit@1.png",
            "snap_name": "梨花带雨 3个等",
            "total_count": 2,
            "prepay_id": null
        },
        {
            "id": 45,
            "order_no": "CB15859143662199",
            "create_time": "2019-11-15 10:45:14",
            "total_price": "0.01",
            "status": 1,
            "snap_img": "http://www.tpthink.cn/images/product-vg@1.png",
            "snap_name": "芹菜 半斤",
            "total_count": 1,
            "prepay_id": null
        }
    ]
}
```



## 创建订单

### 基本信息

- Path：  http://www.tpthink.cn/api/v1/order
- Method：POST
- 接口描述：

### 请求参数

**Headers**

| 参数名称     | 参数值           | 是否必须 | 示例 | 备注 |
| ------------ | ---------------- | -------- | ---- | ---- |
| Content-Type | application/json | 是       |      |      |

**Body**

| 名称         | 类型     | 是否必须 | 示例 | 备注     |
| ------------ | -------- | -------- | ---- | -------- |
| products     | object[] | 是       |      | 商品条目 |
| ├─product_id | int      | 是       |      | 商品id   |
| ├─count      | int      | 是       |      | 商品数量 |

```json
{"products":[{"product_id":8,"count":1},{"product_id":10,"count":2}]}
```



### 返回数据

- 操作成功响应状态码：200

```json
{
    "order_no": "CB15913583627625",
    "order_id": "47",
    "create_time": "2019-11-15 12:15:58",
    "pass": true
}
```



## 查看订单

### 基本信息

- Path：   http://www.tpthink.cn/api/v1/order/46
- Method：GET
- 接口描述：

### 请求参数

**Headers**

| 参数名称 | 参数值  | 是否必须 | 示例                             | 备注     |
| -------- | ------- | -------- | -------------------------------- | -------- |
| token    | token值 | 是       | 34119ed0d7045e1acb63cf066366d772 | 用户令牌 |

### 返回数据

- 操作成功响应状态码：200

```json
{
    "id": 46,
    "order_no": "CB15891253844855",
    "create_time": "2019-11-15 11:38:45",
    "total_price": "0.02",
    "status": 1,
    "snap_img": "http://www.tpthink.cn/images/product-dryfruit@1.png",
    "snap_name": "梨花带雨 3个等",
    "total_count": 2,
    "snap_items": [
        {
            "id": 2,
            "name": "梨花带雨 3个",
            "main_img_url": "http://www.tpthink.cn/images/product-dryfruit@1.png",
            "count": 1,
            "totalPrice": 0.01,
            "price": "0.01",
            "counts": 1
        },
        {
            "id": 22,
            "name": "梅兰清花糕 1个",
            "main_img_url": "http://www.tpthink.cn/images/product-cake-a@3.png",
            "count": 1,
            "totalPrice": 0.01,
            "price": "0.01",
            "counts": 1
        }
    ],
    "snap_address": {
        "name": "李白",
        "mobile": "13012345678",
        "province": "北京市",
        "city": "北京市",
        "country": "朝阳区",
        "detail": "001号",
        "update_time": "1970-01-01 08:00:00"
    }
}
```





# 用户权限

## 获取Token

### 基本信息

- Path： http://www.tpthink.cn/api/v1/token/user
- Method：POST
- 接口描述：

### 请求参数

**Headers**

| 参数名称     | 参数值           | 是否必须 | 示例 | 备注 |
| ------------ | ---------------- | -------- | ---- | ---- |
| Content-Type | application/json | 是       |      |      |

**Body**

| 名称 | 类型   | 是否必须 | 示例                             | 备注             |
| ---- | ------ | -------- | -------------------------------- | ---------------- |
| code | String | 是       | 0014hfIt05zeDj1ByVFt0MB5It04hfIG | 微信登录凭证code |

```json
{"code":"0014hfIt05zeDj1ByVFt0MB5It04hfIG"}
```

### 返回数据

- 操作成功响应状态码：200

```json
{"token":"8741c34e360da3851cc3c6e484619b42"}
```



## Token验证

### 基本信息

- Path： http://www.tpthink.cn/api/v1/token/verify
- Method：POST
- 接口描述：

### 请求参数

**Headers**

| 参数名称     | 参数值           | 是否必须 | 示例 | 备注 |
| ------------ | ---------------- | -------- | ---- | ---- |
| Content-Type | application/json | 是       |      |      |

**Body**

| 名称  | 类型   | 是否必须 | 示例                             | 备注     |
| ----- | ------ | -------- | -------------------------------- | -------- |
| token | String | 是       | b48bfac54c393f26efe559541b0c5d2c | 用户令牌 |

```json
{"token":"b48bfac54c393f26efe559541b0c5d2c"}
```



### 返回数据

- 操作成功响应状态码：200

```json
{"isValid":true}
```



## 获取地址信息

### 基本信息

- Path： http://www.tpthink.cn/api/v1/address
- Method：GET
- 接口描述：

### 请求参数

**Headers**

| 参数名称 | 参数值  | 是否必须 | 示例                             | 备注     |
| -------- | ------- | -------- | -------------------------------- | -------- |
| token    | token值 | 是       | 34119ed0d7045e1acb63cf066366d772 | 用户令牌 |

### 返回数据

- 操作成功响应状态码：200

```json
{
    "name": "李白",
    "mobile": "13012345678",
    "province": "北京市",
    "city": "北京市",
    "country": "朝阳区",
    "detail": "望京001号",
    "update_time": "1970-01-01 08:00:00"
}
```



