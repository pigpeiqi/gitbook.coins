**正式服**：[http://www.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/getRegionServer.c](http://www.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/getRegionServer.c)

**测试服**：[http://test2.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/getRegionServer.c](http://test2.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/getRegionServer.c)

**Method**:`POST`（参数请以`json`格式传递,若字段没有,可不传）

**请求参数**：

| 参数名 | 描述 | 是否必填 |
| :--- | :--- | :--- |
| loginAccount | 卖家99173会员账号 | 是 |
| token | 验证token值 | 是 |

**响应**：

```
{"responseStatus":{"code":200,"message":"操作成功"},"regionServer":[{"gameRegionId":61,"gameRegionName":"广东区","gameServer":[{"gameServerId":62,"gameServerName":"广东1区"},{"gameServerId":63,"gameServerName":"广东2区"},...]},...{"gameRegionId":7257,"gameRegionName":"体验服","gameServer":[{"gameServerId":7264,"gameServerName":"体验服"}]}]}
```

code="200"代表成功 其他代表失败,如失败,失败原因由message 提供

