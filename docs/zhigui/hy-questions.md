



问题：

- 拉起支付 怎么分润？

收到支付成功通知、调用分润接口 ApplyPayShare

- ConfirmPay支付确认接口没有找到？

不需要 

- 是必须先在汇企通注册才能下单？

是

- 注册的时候如果填了三要素或者不填三要素有什么区别？

我们注册的时候只穿userId

- 下单支付的时候的auth_code，从哪来，是绑卡查询返回的那个auth_code吗？

现在都走钱包支付，不需要了

- 统一支付时候传的(商户订单号,同一个商户号下唯一) out_trade_no 和快捷绑卡的 商户签约单号 out_trade_no



![image-20220816114159172](C:/Users/zhangbo/AppData/Roaming/Typora/typora-user-images/image-20220816114159172.png)



![image-20220816114240286](C:/Users/zhangbo/AppData/Roaming/Typora/typora-user-images/image-20220816114240286.png)



- 快捷绑卡是支付的时候可以绑，也可以在企汇通上面绑么？



- 绑卡时候的子商户号 我们需要吗



![image-20220816114106428](C:/Users/zhangbo/AppData/Roaming/Typora/typora-user-images/image-20220816114106428.png)



- merch_user_id api是16位，我传的是我们平台的用户id 36位有问题吗

