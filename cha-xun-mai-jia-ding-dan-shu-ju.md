**正式服**：[http://www.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/orderPages.c](http://www.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/orderPages.c)

**测试服**：[http://test2.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/orderPages.c](http://test2.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/orderPages.c)

**Method**:`POST`（参数请以`json`格式传递,若字段没有,可不传）

**请求参数**：

| 参数名 | 描述 | 是否必填 |
| :--- | :--- | :--- |
| page | 要获取第几页数据，默认值1 | 否 |
| pageSize | 每页获取几条数据，默认值20，最大50 | 否 |
| gameRegionId | 游戏大区ID | 否 |
| gameServerId | 游戏服务器ID | 否 |
| gameAccount | 游戏账号 | 否 |
| loginAccount | 卖家99173会员账号 | 是 |
| token | 验证token值 | 是 |

**响应**`JSON`**数据**：

```
{"responseStatus":{"code":200,"message":"操作成功"},"repositoryList":{"totalCount":2,"pageSize":20,"currPage":1,"totalPage":1,"data":[{"id":10919,"productId":14274,"gameRegionId":61,"gameRegionName":"广东区","gameServerId":62,"gameServerName":"广东1区","orderMoney":10000,"saleType":2,"orderId":"GG201811221357074580","recRegionId":61,"recRegionName":"广东区","recServerId":63,"recServerName":"广东2区","recRoleName":"1","buyerPhone":"15385283623","buyerQQ":"3232323","payTime":"2018-11-22 13:57:09","status":2},{...}]}}
```

| 参数 | 说明 |
| :--- | :--- |
| responseStatus | responseStatus.code="00"代表成功 responseStatus.message="操作成功" 若失败message返回对应错误信息 code为错误码 |
| repositoryList.data | 库存数据 |
| repositoryList.pageSize | 每页几条数据 |
| srepositoryList.currPage | 当前是第几页 |
| srepositoryList.totalCount | 总记录数 |
| repositoryList.totalPage | 总页数 |

**注**：status为订单状态，0待付款，1交易中，2交易成功，3交易失败，4订单删除。响应参数含义请在5中查看；

