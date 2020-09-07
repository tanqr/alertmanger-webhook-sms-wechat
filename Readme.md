## 工具说明
Prometheus的告警消息通过Alertmanager发送消息，支持邮件，企业微信，webhook等方式。本工具是通过webhook的方式接收alertmanager的告警消息，再通过自定义的格式化的方式将告警发送给企业微信和短信。
  
由于短信发送由于服务商不同，发送方式不统一，但大多数是以post传参的方式发送，本工具为适配各种Post方式，传参以及参数值都可以自定义，参数数量也不限。

本工具默认开启企业微信和短信，如不需要，在alertmanager发送消息时不要带手机号或是企业微信的参数。
## 使用说明

### 启动本工具
### alertmanager配置


## 参数说明


- "W", 默认："https://qyapi.weixin.qq.com",说明： "企业微信地址，可以是代理,可以加上端口"
- "P", 默认："5011", 说明："server port "
- "d", 默认：false, 说明："debug mode，暂时没用"
- "A", 默认："100", 说明："Value四舍五入的精度"
- "smsurl", 默认："http://test.sms.com:8080/emas/simpleinter/sendSMS", 说明："发送短信的服务地址"
- "smsparamkey", 默认："appid,timestamp,sign", 说明："发送短信的post 参数"
- "content", 默认："content", 说明："发送短信的post 参数:数据部分 "
- "phone", 默认："mobiles", 说明："发送短信的post 参数:手机KEY参数 "
