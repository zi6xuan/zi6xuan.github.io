## Jason
---
### 关于VoIP推送的一些问题
- VoIP推送到达设备时，必须要提交给系统来显示电话到达，否则大量未上报的VoIP推送会导致后续的推送优先级越来越低
- 如果发生了大量未上报VoIP推送的情况，可以通过完全卸载App并重新安装来解决
- apple服务器的请求设置里 apns-expiration 最好设置为0，应该立即丢弃延时的Voip推送防止累计性问题导致优先度降低
- apple服务器的请求设置里 apns-collapse-id 由于过期或者延时的VoIP最好时丢弃处理，所以不需要集合再发送
### 关于Android 网页和app之间钥匙串密码共享的问题
- android设置完App和网站的必要数据后，需要通过googlePlay发不到alpha或者beta版本才可以进行关联测试。内部测试不适用。
---
