**正式服**：[http://www.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/orderDetail.c](http://www.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/orderDetail.c)

**测试服**：[http://test2.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/orderDetail.c](http://test2.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/orderDetail.c)

**Method**:`POST`（参数请以`json`格式传递,若字段没有,可不传）

**请求参数**：

| 参数名 | 描述 | 是否必填 |
| :--- | :--- | :--- |
| productId | 商品ID | 是 |
| orderId | 订单编号 | 是 |
| loginAccount | 卖家99173会员账号 | 是 |
| token | 验证token值 | 是 |

**响应**`JSON`**数据**：

```php
{
  "responseStatus": {
  "code": 200,                                            //响应状态码
  "message": "操作成功"                                    //响应提示信息
  }
  "repositoryData": {
  "id": 10919,                                            //订单ID
  "productId": 14274,                                     //商品ID
  "gameRegionId": 61,                                     //游戏大区id
  "gameRegionName": "广东区",                              //游戏大区名称
  "gameServerId": 62,                                     //服务器大区id
  "gameServerName": "广东1区",                             //服务器大区名称
  "orderMoney": 300,                                      //订单总金额，单位：元
  "saleType": 2,                                          //出售方式（1寄售交易，2担保交易）
  "orderId": "GG201811221357074580",                      //订单编号
  "recRegionId": 61,                                      // 收货角色大区id
  "recRegionName": "广东区",                               //收货角色大区名称
  "recServerId": 63,                                      //收货角色服务器大区id
  "recServerName": "广东2区",                              //收货角色服务器大区名称
  "recRoleName": "大将军",                                 // 收货角色名
  "buyerPhone": "15385283623",                            //买家电话
  "buyerQQ": "3232323",                                   //买家QQ
  "payTime": "2018-11-22 13:57:09",                       // 付款时间
  "status": 2,                                            //订单状态
  "createTime": "2018-11-22 13:57:07",                    // 下单时间
  "productPrice": 100,                                    // 商品价格
  "productName": "1000万金币=100元",                       // 商品标题
  "productStock": 98,                                     //库存
  "deliveryType": 1,                                      //发货方式（1当面发货，2邮寄发货，3拍卖发货）
  "dealNum": 3000,                                        //交易商品数量，单位：万金币
  "buyNumber" : 3,                                        //购买商品件数
  "unit": "万金币",                                        //单位
  "productType": "游戏币"                                  //商品类型
  }
}
```

**注**：status为订单状态，0待付款，1交易中，2交易成功，3交易失败，4订单删除；code="200"代表成功 其他代表失败,如失败,失败原因由message 提供；

