**正式服**：[http://www.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/operateCoins.c](http://www.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/operateCoins.c)

**测试服**：[http://test2.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/operateCoins.c](http://test2.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/operateCoins.c)

**Method**:`POST`（参数请以`json`格式传递,若字段没有,可不传）

**请求参数**：

| 参数名 | 描述 | 是否必填 |
| :--- | :--- | :--- |
| loginAccount | 卖家99173会员账号 | 是 |
| token | 验证token值 | 是 |
| id | 商品id | 是 |
| price | 单件商品价格：单位元 | 是 |
| itemNum | 单件商品数量 | 是 |
| stockNum | 库存数量 | 是 |
| productId | 商品编号 | 是 |

**响应**：

{"responseStatus":{"code":200,"message":"修改成功"}}，code="200"代表成功 其他代表失败,如失败,失败原因由message 提供；

