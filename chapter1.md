# 

**正式服**：[http://www.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/accessToken.c](http://www.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/accessToken.c)

**测试服**：[http://test2.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/accessToken.c](http://test2.99173.com/gamegold-facade-frontend/services/v1.0/mallOpen/accessToken.c)

**Method**：`POST`（参数请以`json`格式传递,若字段没有,可不传）

**请求参数**：

| 参数名 | 描述 | 是否必填 |
| :--- | :--- | :--- |
| firmSecret | 厂商秘钥，联系99173客户获取并自行保存 | 是 |
| appid | 卖家99173授权码,请卖家联系99173客服获取并自行保存 | 是 |
| sign | MD5加密后字符串 | 是 |
| loginAccount | 卖家99173账号，请卖家自行注册为99173，并完善会员信息 | 是 |

**注**：字符串encryptKey为加密秘钥仅双方可知 测试用 加密秘钥 encryptKey=!rBq^EA

sign为字符串：sign=firmSecret&appid&loginAccount&encryptKey&99173 MD5加密之后的值

正式服注册会员地址：[http://www.99173.com/register.html](http://www.99173.com/register.html)

测试服注册会员地址：[http://test2.99173.com/register.html](http://test2.99173.com/register.html)

**响应**:

{"responseStatus":{"code":200,"message":"操作成功"},"token":"4062fb7505c108e42ef9290a1f4f681e"}

code="200"代表成功 其他代表失败,如失败,失败原因由message 提供；

当有请求返回 message提示token不存在或者已过期时,需要重新注册令牌效验,其他接口中token均为此接口返回token，请调用方法自行保存,其他接口中token均为此值

