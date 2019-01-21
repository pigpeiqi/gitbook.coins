**正式服**：[http://www.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/coinsPages.c](http://www.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/coinsPages.c)

**测试服**：[http://test2.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/coinsPages.c](http://test2.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/coinsPages.c)

**Method**：`POST`（参数请以`json`格式传递,若字段没有,可不传）

**请求参数**：

| 参数名 | 描述 | 是否必填 |
| :--- | :--- | :--- |
| page | 要获取第几页数据，默认值1 | 否 |
| pageSize | 每页获取几条数据，默认值20,最大50 | 否 |
| gameRegionId | 游戏大区ID | 否 |
| gameServerId | 游戏服务器ID | 否 |
| gameAccount | 游戏账号 | 否 |
| loginAccount | 卖家99173会员账号 | 是 |
| token | 验证token值 | 是 |
| productId | 商品编号 | 否 |

**响应**`JSON`**数据**：

```
{"responseStatus":{"code":200,"message":"操作成功"},"repositoryList":{"totalCount":3,"pageSize":20,"currPage":1,"totalPage":1,"data":[{"id":14273,"productId":"SP201811220927026860","saleType":1,"gameRegionid":61,"gameRegionName":"广东区","gameServerId":62,"gameServerName":"广东1区","unitNum":1000,"deliveryType":1,"Unit":"千金币","Title":"1000万金币=100","unitPrice":10000,"stockNum":100,"gameAccount":"1",...},{...},{...}]}}
```

| 参数 | 说明 |
| :--- | :--- |
| responseStatus | responseStatus.code="200"代表成功 responseStatus.message="操作成功" 若失败message返回对应错误信息 code为错误码 |
| repositoryList.data | 库存数据 |
| repositoryList.pageSize | 每页几条数据 |
| srepositoryList.currPage | 当前是第几页 |
| srepositoryList.totalCount | 总记录数 |
| repositoryList.totalPage | 总页数 |
| repositoryList.data.id | 商品ID |
| repositoryList.data.productId | 商品编号 |
| repositoryList.data.coinsUnit | 游戏币单位 |
| repositoryList.data.productName | 商品标题 |
| repositoryList.data.status | 商品状态（1出售中，2待支付，3交易中，4已售完,5下架，7删除） |

**注**：响应参数含义与添加库存时字段含义相同中；

