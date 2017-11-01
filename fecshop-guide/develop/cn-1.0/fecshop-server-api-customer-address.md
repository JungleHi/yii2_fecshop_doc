Api- Customer address 列表
================

> 账户中心，获取用户的address列表的api

URL: `/customer/address/index`

格式：`json`

方式：`get`


一：请求部分
---------

#### 1.Request Header


| 参数名称          | 是否必须    |  类型        |  描述     |
| ------------------| -----:      | :----:       |:----:     |
| access-token      | 必须        |   String     | 从localStorage取出来的值，识别用户登录状态的标示，用户登录成功，服务端返回access-token，VUE保存到localStorage中，在下一次请求从localStorage取出来放到request header中   |
| fecshop-uuid      | 必须        |   String     | 从localStorage取出来的值，用户的唯一标示，VUE第一次访问服务端，服务端会返回fecshop-uuid ，VUE将其保存到本地，后面的每一次请求都需要加上fecshop-uuid    |
| fecshop-currency  | 必须        |   String     | 从localStorage取出来的值，当前的货币值  |
| fecshop-lang      | 必须        |   String     | 从localStorage取出来的值，当前的语言code  |


#### 2.Request Body Form-Data：


无


**请求参数示例如下：**

```
无
```

二：返回部分
----------

#### 1.Reponse Header

| 参数名称          | 是否必须    |  类型        |  描述     |
| ------------------| -----:      | :----:       |:----:     |
| access-token      | 选填        |   String     | 用户登录成功，服务端返回access-token，VUE保存到localStorage中，在下一次请求从localStorage取出来放到request header中   |
| fecshop-uuid      | 必须        |   String     | 用户的唯一标示，VUE第一次访问服务端，服务端会返回fecshop-uuid ，VUE将其保存到本地，后面的每一次请求都需要加上fecshop-uuid    |

#### 2.Reponse Body Form-Data：

格式：`json`

| 参数名称        | 是否必须    |  类型       |  描述        |
| ----------------| -----:      | :----:      |:----:        | 
| code            | 必须        |   Number    | 返回状态码，200 代表完成，完整的返回状态码详细参看:[Api- 状态码](fecshop-server-return-code.md) |
| message         | 必须        |   String    | 返回状态字符串描述  |
| data            | 必须        |   Array     | 返回详细数据        |

返回数据举例：

```
{
    "code": 200,
    "message": "process success",
    "data": {
        "addressList": [
            {
                "address_id": "117",
                "first_name": "111",
                "email": "34343@3232.com",
                "last_name": "222",
                "company": null,
                "telephone": "3232",
                "fax": null,
                "street1": "3232",
                "street2": "3232",
                "city": "3232",
                "state": "BJ",
                "zip": "ewewew",
                "country": "CN",
                "customer_id": "46",
                "created_at": "1506397313",
                "updated_at": "1509161659",
                "is_default": "2",
                "stateName": "北京市",
                "countryName": "China"
            },
            {
                "address_id": "118",
                "first_name": "2121",
                "email": "fdfd@3232.com",
                "last_name": "2121",
                "company": null,
                "telephone": "2121",
                "fax": null,
                "street1": "2121",
                "street2": "2121",
                "city": "2121",
                "state": "NO",
                "zip": "2121",
                "country": "AT",
                "customer_id": "46",
                "created_at": "1506397526",
                "updated_at": "1509158174",
                "is_default": "1",
                "stateName": "Niederösterreich",
                "countryName": "Austria"
            }
        ]
    }
}
```