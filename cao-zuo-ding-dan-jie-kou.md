**正式服**：[http://www.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/operateOrder.c](http://www.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/operateOrder.c)

**测试服**：[http://test2.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/operateOrder.c](http://test2.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/operateOrder.c)

**Method**:`POST`（参数请以`json`格式传递,若字段没有,可不传）

**请求参数**：

| 参数名 | 描述 | 是否必填 |
| :--- | :--- | :--- |
| loginAccount | 卖家99173会员账号 | 是 |
| token | 验证token值 | 是 |
| orderId | 订单号 | 是 |
| id | 订单id | 是 |
| type | 数字1：修改订单为交易完成；数字2：退款 | 是 |

**响应值**：{"responseStatus":{"code":200,"message":"订单交易成功"}}，code="200"代表成功 其他代表失败,如失败,失败原因由message 提供；

