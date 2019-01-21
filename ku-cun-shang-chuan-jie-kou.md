**正式服**：[http://www.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/relCoins.c](http://www.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/relCoins.c)

**测试服**：[http://test2.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/relCoins.c](http://test2.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/relCoins.c)

**Method**：`POST`（参数请以`json`格式传递）

**请求参数**：

```php
{
    "loginAccount": "testLoginAccount",                              //卖家99173会员账号【必填】
    "token": "0be271a0c0724e59a0fb2b25223487c0",                     //token【必填】
    "repositories": [{
        "gameAccount": "p_85i2ysq3q",                                //游戏账号【寄售必填】
        "gamePassWord": "123456",                                    //游戏账号密码【寄售必填】
        "saleType": 1,                                               //出售方式（1寄售交易，2担保交易）【必填】
        "deliveryType": "1"                                          // 发货方式（1当面发货，2邮寄发货，3拍卖发货）【必填】
        "itemNum": "1000"                                            //单件商品数量，单位：万金币【必填】
        "price": "100",                                              //单件商品价格 单位：元【必填】
        "stockNum": "50",                                            //上传库存数量（最大100件)【必填】
        "gameRoleName": "大将军",                                     //出货角色 【必填】
        "secondaryPassword ": "0",                                    //二级密码 【选填】
        "depotPassword": "0",                                         //仓库密码【选填】
        "goodsPlace": "背包",                                         //商品存放处【选填】（背包，仓库，账号仓库，邮箱，拍卖行）【选填】
        "phoneNum": "13966666666",                                    //手机号 【必填】
        "qqNum": "111111",                                            //QQ号【必填】
        "tradeStart": "1",                                            //方便交易开始时间0~23，例：0 代表00 : 00,23代表23 : 00 ',【担保出货时必填写】
        "tradeEnd": "24"                                              //方便交易开始时间0~23，例：0代表00:00,23代表23:00',【担保出货时必填写】
        "gameRegionId": "61"                                          //游戏大区id
        "gameRegionName": "广东区"                                     //游戏大区名称
        "gameServerId": "62"                                          //服务器大区id
        "gameServerName": "广东1区"                                    //服务器大区名称
    }]
}
```

**注意**：请保证属性名大小写一致。其中游戏区服信息，请根据[**获取游戏区服接口**](https://631775723.gitbook.io/coins/huo-qu-you-xi-qu-fu)。自行获取并保存

**响应值**：{"responseStatus":{"code":200,"message":"发布成功"}}，code="200"代表成功 其他代表失败,如失败,失败原因由message 提供；

