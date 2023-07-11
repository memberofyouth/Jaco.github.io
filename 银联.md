```
	
验签未通过
2022-09-24 00:58:01	
待签名字符串：JL=DbkZ&billDate=2022-09-24&billDesc=中保付测试商户(中保付测试商户)&billNo=8888b4f-178e-4a04-8ad4-79fa0&billPayment={"payTime":"2022-09-24 00:57:58","paySeqId":"01175500115N","invoiceAmount":20,"settleDate":"2022-09-24","buyerId":"o8wNP0agr1roauVXTWpuLhT2VL0M","receiptAmount":20,"totalAmount":20,"billBizType":"bills","buyerPayAmount":20,"targetOrderId":"4200001567202209249273711154","merOrderId":"8888b4f-178e-4a04-8ad4-79fa00","status":"TRADE_SUCCESS","targetSys":"WXPay"}&billQRCode=https://qr-test3.chinaums.com/bills/qrCode.do?id=10002209241195738009194596&billStatus=PAID&counterNo=868b0b4f178e4a048ad479fa01981786&createTime=2022-09-24 00:57:38&instMid=QRPAYDEFAULT&mchntUuid=6d47dc12a4c847eaba2eb456d201d5cd&memberId=fc95d158f8e54fe7ba2e923961440652&merName=中保付测试商户(中保付测试商户)&mid=898201612345678&notifyId=7df96f1d-0a73-41af-8c33-ec1ebe968dd7&qrCodeId=10002209241195738009194596&qrCodeType=BILLPAY&receiptAmount=20&seqId=01175500115N&signType=SHA256&subInst=100200&tid=88880001&totalAmount=20impARTxrQcfwmRijpDNCw6hPxaWCddKEpYxjaKXDhCaTCXJ6
2022-09-24 00:58:01	


081149D185636E219BCAA1269E2D61B382907CE141DCE4E36D85B1B4B440DF76
2022-09-24 00:58:01	
params:{billPayment={"payTime":"2022-09-24 00:57:58","paySeqId":"01175500115N","invoiceAmount":20,"settleDate":"2022-09-24","buyerId":"o8wNP0agr1roauVXTWpuLhT2VL0M","receiptAmount":20,"totalAmount":20,"billBizType":"bills","buyerPayAmount":20,"targetOrderId":"4200001567202209249273711154","merOrderId":"8888b4f-178e-4a04-8ad4-79fa00","status":"TRADE_SUCCESS","targetSys":"WXPay"}, 

qrCodeId=10002209241195738009194596, JL=DbkZ, counterNo=868b0b4f178e4a048ad479fa01981786, billDesc=中保付测试商户(中保付测试商户), sign=081149D185636E219BCAA1269E2D61B382907CE141DCE4E36D85B1B4B440DF76, merName=中保付测试商户(中保付测试商户), mid=898201612345678, billDate=2022-09-24, qrCodeType=BILLPAY, mchntUuid=6d47dc12a4c847eaba2eb456d201d5cd, tid=88880001, instMid=QRPAYDEFAULT, receiptAmount=20, totalAmount=20, createTime=2022-09-24 00:57:38, billStatus=PAID, signType=SHA256, notifyId=7df96f1d-0a73-41af-8c33-ec1ebe968dd7, billNo=8888b4f-178e-4a04-8ad4-79fa0, subInst=100200, seqId=01175500115N, billQRCode=https://qr-test3.chinaums.com/bills/qrCode.do?id=10002209241195738009194596, memberId=fc95d158f8e54fe7ba2e923961440652}




2022-09-24 00:58:01.124  INFO 6 --- [nio-8080-exec-1] c.z.s.o.controller.PayNotifyController   : request:{"billPayment":["{\"payTime\":\"2022-09-24 00:57:58\",\"paySeqId\":\"01175500115N\",\"invoiceAmount\":20,\"settleDate\":\"2022-09-24\",\"buyerId\":\"o8wNP0agr1roauVXTWpuLhT2VL0M\",\"receiptAmount\":20,\"totalAmount\":20,\"billBizType\":\"bills\",\"buyerPayAmount\":20,\"targetOrderId\":\"4200001567202209249273711154\",\"merOrderId\":\"8888b4f-178e-4a04-8ad4-79fa00\",\"status\":\"TRADE_SUCCESS\",\"targetSys\":\"WXPay\"}"],"qrCodeId":["10002209241195738009194596"],"JL":["DbkZ"],"counterNo":["868b0b4f178e4a048ad479fa01981786"],"billDesc":["中保付测试商户(中保付测试商户)"],"sign":["081149D185636E219BCAA1269E2D61B382907CE141DCE4E36D85B1B4B440DF76"],"merName":["中保付测试商户(中保付测试商户)"],"mid":["898201612345678"],"billDate":["2022-09-24"],"qrCodeType":["BILLPAY"],"mchntUuid":["6d47dc12a4c847eaba2eb456d201d5cd"],"tid":["88880001"],"instMid":["QRPAYDEFAULT"],"receiptAmount":["20"],"totalAmount":["20"],"createTime":["2022-09-24 00:57:38"],"billStatus":["PAID"],"signType":["SHA256"],"notifyId":["7df96f1d-0a73-41af-8c33-ec1ebe968dd7"],"billNo":["8888b4f-178e-4a04-8ad4-79fa0"],"subInst":["100200"],"seqId":["01175500115N"],"billQRCode":["https://qr-test3.chinaums.com/bills/qrCode.do?id=10002209241195738009194596"],"memberId":["fc95d158f8e54fe7ba2e923961440652"]}
2022-09-24 00:58:01	
2022-09-24 00:58:01.123  INFO 6 --- [nio-8080-exec-1] c.z.s.c.interceptor.TokenInterceptor     : request uri:/payment-callback/union/notify/paid
2022-09-24 00:57:33	






验签未通过
2022-09-24 00:57:33	
待签名字符串：Dv=kXXE&billDate=2022-09-24&billDesc=中保付测试商户(中保付测试商户)&billNo=8888aa1-5572-47ea-8d48-0ee2d&billPayment={"payTime":"2022-09-24 00:51:19","paySeqId":"01175500114N","invoiceAmount":20,"settleDate":"2022-09-24","buyerId":"o8wNP0agr1roauVXTWpuLhT2VL0M","receiptAmount":20,"totalAmount":20,"billBizType":"bills","buyerPayAmount":20,"targetOrderId":"4200001584202209243469551584","merOrderId":"8888aa1-5572-47ea-8d48-0ee2d0","status":"TRADE_SUCCESS","targetSys":"WXPay"}&billQRCode=https://qr-test3.chinaums.com/bills/qrCode.do?id=10002209241994954000192660&billStatus=PAID&counterNo=a0283aa1557247ea8d480ee2dd288950&createTime=2022-09-24 00:49:54&instMid=QRPAYDEFAULT&mchntUuid=6d47dc12a4c847eaba2eb456d201d5cd&memberId=fc95d158f8e54fe7ba2e923961440652&merName=中保付测试商户(中保付测试商户)&mid=898201612345678&notifyId=93e5398a-5b74-4475-826a-85c79e3a92e3&qrCodeId=10002209241994954000192660&qrCodeType=BILLPAY&receiptAmount=20&seqId=01175500114N&signType=SHA256&subInst=100200&tid=88880001&totalAmount=20impARTxrQcfwmRijpDNCw6hPxaWCddKEpYxjaKXDhCaTCXJ6
2022-09-24 00:57:33	
EF7B8F6A7EB3E562A4E8B0156DE1A204188815F59CF91A9183346D2FAB7C2EA2
2022-09-24 00:57:33	
params:{billPayment={"payTime":"2022-09-24 00:51:19","paySeqId":"01175500114N","invoiceAmount":20,"settleDate":"2022-09-24","buyerId":"o8wNP0agr1roauVXTWpuLhT2VL0M","receiptAmount":20,"totalAmount":20,"billBizType":"bills","buyerPayAmount":20,"targetOrderId":"4200001584202209243469551584","merOrderId":"8888aa1-5572-47ea-8d48-0ee2d0","status":"TRADE_SUCCESS","targetSys":"WXPay"}, qrCodeId=10002209241994954000192660, counterNo=a0283aa1557247ea8d480ee2dd288950, billDesc=中保付测试商户(中保付测试商户), sign=EF7B8F6A7EB3E562A4E8B0156DE1A204188815F59CF91A9183346D2FAB7C2EA2, merName=中保付测试商户(中保付测试商户), mid=898201612345678, billDate=2022-09-24, qrCodeType=BILLPAY, mchntUuid=6d47dc12a4c847eaba2eb456d201d5cd, tid=88880001, instMid=QRPAYDEFAULT, receiptAmount=20, totalAmount=20, Dv=kXXE, createTime=2022-09-24 00:49:54, billStatus=PAID, signType=SHA256, notifyId=93e5398a-5b74-4475-826a-85c79e3a92e3, billNo=8888aa1-5572-47ea-8d48-0ee2d, subInst=100200, seqId=01175500114N, billQRCode=https://qr-test3.chinaums.com/bills/qrCode.do?id=10002209241994954000192660, memberId=fc95d158f8e54fe7ba2e923961440652}
2022-09-24 00:57:33	
2022-09-24 00:57:33.544  INFO 6 --- [io-8080-exec-10] c.z.s.o.controller.PayNotifyController   : request:{"billPayment":["{\"payTime\":\"2022-09-24 00:51:19\",\"paySeqId\":\"01175500114N\",\"invoiceAmount\":20,\"settleDate\":\"2022-09-24\",\"buyerId\":\"o8wNP0agr1roauVXTWpuLhT2VL0M\",\"receiptAmount\":20,\"totalAmount\":20,\"billBizType\":\"bills\",\"buyerPayAmount\":20,\"targetOrderId\":\"4200001584202209243469551584\",\"merOrderId\":\"8888aa1-5572-47ea-8d48-0ee2d0\",\"status\":\"TRADE_SUCCESS\",\"targetSys\":\"WXPay\"}"],"qrCodeId":["10002209241994954000192660"],"counterNo":["a0283aa1557247ea8d480ee2dd288950"],"billDesc":["中保付测试商户(中保付测试商户)"],"sign":["EF7B8F6A7EB3E562A4E8B0156DE1A204188815F59CF91A9183346D2FAB7C2EA2"],"merName":["中保付测试商户(中保付测试商户)"],"mid":["898201612345678"],"billDate":["2022-09-24"],"qrCodeType":["BILLPAY"],"mchntUuid":["6d47dc12a4c847eaba2eb456d201d5cd"],"tid":["88880001"],"instMid":["QRPAYDEFAULT"],"receiptAmount":["20"],"totalAmount":["20"],"Dv":["kXXE"],"createTime":["2022-09-24 00:49:54"],"billStatus":["PAID"],"signType":["SHA256"],"notifyId":["93e5398a-5b74-4475-826a-85c79e3a92e3"],"billNo":["8888aa1-5572-47ea-8d48-0ee2d"],"subInst":["100200"],"seqId":["01175500114N"],"billQRCode":["https://qr-test3.chinaums.com/bills/qrCode.do?id=10002209241994954000192660"],"memberId":["fc95d158f8e54fe7ba2e923961440652"]}
```























































![image-20220921171136530](C:/Users/zhangbo/AppData/Roaming/Typora/typora-user-images/image-20220921171136530.png)





redis单节点：8.142.103.74:32639    MTIzNDUzCg==



mysql：8.142.103.74:30017    root /  QqWxTh2J!YpMdhs



【元枢】您的商户信息已提交成功，请前往我的钱包进行签约。 

【元枢】您的商户信息已提交失败，失败原因：[原因替换]。









user_code (银联uid)



usermerNo （银联返回）



获取银联付款二维码

（H5、pc、app）



pc 段让前端生产二维码





支付是否能重复支付

用户商户号？

用户都需要开通子商户吗？

自助进件 进度查询？



单位？

100元怎么 分？



回调api 



挂售、回调、

卖方挂售多支付方式

银联支付



买方支付

支付成功发短信包含收款渠道



银联对接 t+1 第二天 1点到3点





银联接口

client.go

response.go



![image-20220920182839319](C:/Users/zhangbo/AppData/Roaming/Typora/typora-user-images/image-20220920182839319.png)



paymethod  传后面引号内

```
const (
   UnionPayPCQrCode    = "UnionPayPCQrCode" // 银联CB扫描二维码支付
   UnionPayH5Ali       = "UPH5Ali"          // 8 银联 支付宝H5支付：
   UnionPayH5Wx        = "UPH5Wx"           // 9 银联 微信H5支付：
   UnionPayH5Ysf       = "UPH5Ysf"          // 10 银联 银联云闪付：
   UnionPayH5WxXcx     = "UPH5WxXcx"        // 11 银联 微信H5转小程序支付：
   UnionPayAppAliXcx   = "UPAppAliXcx"      // 12 银联APP支付-支付宝小程序
   UnionPayAppYsf      = "UPAppYsf"         // 13 银联APP支付-云闪付
   UnionPayAppApplePay = "UPAppApplePay"    // TBD 待定 银联APP支付-ApplePay 暂不支持
)
```



![image-20220920184511093](C:/Users/zhangbo/AppData/Roaming/Typora/typora-user-images/image-20220920184511093.png)





```java
curl -X POST -H "Content-type: application/json" -d \"{\"orderNo\": \"123123\",\"buyerCode\": \"123\",\"platformAmount\": \"1\",\"totalAmount\": \"11\",\"billDate\": \"2022-09-21T00:00:00.000Z\",\"expireAt\": \"2022-09-21T12:00:00.000Z\",\"suborders\": [{\"Mid\": \"11111\",\"TotalAmount\": \"10\"}]}\" http://localhost:9090/invoke/UnionPayService.UnionPayService.GetPCPayQrCode
```