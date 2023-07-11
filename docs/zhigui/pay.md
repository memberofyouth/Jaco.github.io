

![image-20220928141738795](C:/Users/zhangbo/AppData/Roaming/Typora/typora-user-images/image-20220928141738795.png)









Zhigui123

https://www.heepay.com/Index.aspx









```json
 {"return_code":"FAIL","return_msg":"单据不存在","sign":"9F0D15C3F356680E5F91817A2BB08812"}
```



```json

{"return_code":"SUCCESS","return_msg":"提交成功","result_code":"SUCCESS","hy_bill_no":"H2208299703901AR","out_trade_no":"6358045aa42a484f848aca6c19d8638c-1-1-1","bill_info":"{\"trade_type\":\"5\",\"hy_bill_no\":\"H2208299703901AR\",\"bill_status\":\"Success\",\"trade_amt_fen\":\"20\",\"fee_amt_fen\":\"0\",\"real_amt_fen\":\"20\",\"deal_time\":\"20220829005735\",\"pay_method\":\"0\"}","sign":"05B62990C223ABD77767A7101DFE7553"}
```

```

{"return_code":"SUCCESS","return_msg":"提交成功","result_code":"SUCCESS","hy_bill_no":"H2208290086702AR","out_trade_no":"6ee4a5305eb175591ed377bbe1e8274d1","bill_info":"{\"trade_type\":\"5\",\"hy_bill_no\":\"H2208290086702AR\",\"bill_status\":\"Failure\",\"trade_amt_fen\":\"0\",\"fee_amt_fen\":\"0\",\"deal_time\":\"20220829144348\",\"fail_reason\":\"YBLA01928725账户余额不足 (PB520011)\",\"pay_method\":\"63\"}","sign":"91CF174E9EE1C6121D94A7146E096145"}
2022-08-29 14:44:05	
请求参数：{"method":"v1.BillInfo","version":"1.0","api_type":1,"app_id":"hyp2208171243760001955850C9A2350","charset":"utf-8","owner_uid":"1243762139077","sign_type":"MD5","timestamp":"20220829144405","biz_content":"{\"out_trade_no\":\"6ee4a5305eb175591ed377bbe1e8274d1\",\"trade_type\":5}","sign":"6A038A681E4803316CFD10E24052131E"}
```





汇元支付



新快捷绑卡

签名参数：api_type=1&app_id=hyp200428107197000024987419303A3&biz_content={"encrypt_data":"907a15b09925428606957c53b866c9237c20d696aef8e4df6728027a4a7c96fbab15778d7cb2019134b442289c679a308b1c53560a11aa76982d8797d3c48dbd15c09fb6da171ccb84ece3cdd0f3e66e67e45f27969db1c1912a96d347004af46348d6028f846215694c0b07a3e6a3f489b5cac8b91b03db03932032c11f2e39cf44ba8d11dc9a08d173a61455b2cfa4e98fe04a212896360835ecfea7e5be009c7833f1bfd1345ed173a61455b2cfa4e98fe04a2128963630f50b060dec43e3"}&charset=utf-8&method=/v1/HeepayAuthPageSign&owner_uid=1071972125197&sign_type=MD5&timestamp=20220815141952&version=1.0&key=F8CF6A3E07114934AE684638
签名结果：68B79FD552B5B8B7E11058764470CF88
请求参数：{"method":"/v1/HeepayAuthPageSign","version":"1.0","api_type":1,"app_id":"hyp200428107197000024987419303A3","charset":"utf-8","owner_uid":"1071972125197","sign_type":"MD5","timestamp":"20220815141952","biz_content":"{\"encrypt_data\":\"907a15b09925428606957c53b866c9237c20d696aef8e4df6728027a4a7c96fbab15778d7cb2019134b442289c679a308b1c53560a11aa76982d8797d3c48dbd15c09fb6da171ccb84ece3cdd0f3e66e67e45f27969db1c1912a96d347004af46348d6028f846215694c0b07a3e6a3f489b5cac8b91b03db03932032c11f2e39cf44ba8d11dc9a08d173a61455b2cfa4e98fe04a212896360835ecfea7e5be009c7833f1bfd1345ed173a61455b2cfa4e98fe04a2128963630f50b060dec43e3\"}","sign":"68B79FD552B5B8B7E11058764470CF88"}
返回结果：{"return_code":"SUCCESS","return_msg":"调用成功","result_code":"SUCCESS","result_msg":"请求成功","redirect_url":"http://211.103.157.45/PayHeepay/API/PageSign/www/index.html#/?pre_sign_uid=sn-220815141910021e9c1a4038804e6c8addd0e938e4b987D&merch_id=2125197&timespan=637961699972780161&sign=d4293cd67a2f73d66a88c1faf04402cc","sign":"52580052F283FB6B931FAA9E9606C197"}



注册

签名参数：api_type=1&app_id=hyp200428107197000024987419303A3&biz_content={"region_code":"","user_address":"","user_code":"fc95d158f8e5"}&charset=utf-8&method=/v1/LoginWallet&owner_uid=1071972125197&sign_type=MD5&timestamp=20220816181903&version=1.0&key=F8CF6A3E07114934AE684638
签名结果：3906E98EB8018892685AE6F6CEA4B46F
请求参数：{"method":"/v1/LoginWallet","version":"1.0","api_type":1,"app_id":"hyp200428107197000024987419303A3","charset":"utf-8","owner_uid":"1071972125197","sign_type":"MD5","timestamp":"20220816181903","biz_content":"{\"region_code\":\"\",\"user_address\":\"\",\"user_code\":\"fc95d158f8e5\"}","sign":"3906E98EB8018892685AE6F6CEA4B46F"}
返回结果：{"return_code":"SUCCESS","return_msg":"调用成功","result_code":"SUCCESS","result_msg":"申请成功","user_code":"fc95d158f8e5","redirect_url":"https://demo.heemoney.com/yunbiz/Account/Register/Index?token=8D0A035F6F76B31690DBF8A34E6B817ECB562DB955340F6B42312D83FFD540E3C5453C13E33253C0","is_new_user":"1","sign":"2EA65AD72CCFBA2A8BE4B76AD9F4F2B0"}



签名参数：api_type=1&app_id=hyp200428107197000024987419303A3&biz_content={"region_code":"","user_address":"","user_code":"fc95d158f8e54fe7ba2e923961440652"}&charset=utf-8&method=/v1/LoginWallet&owner_uid=1071972125197&sign_type=MD5&timestamp=20220817111630&version=1.0&key=F8CF6A3E07114934AE684638
签名结果：346BEE8C66AC85DC04ED1B9D99A5CD6C
请求参数：{"method":"/v1/LoginWallet","version":"1.0","api_type":1,"app_id":"hyp200428107197000024987419303A3","charset":"utf-8","owner_uid":"1071972125197","sign_type":"MD5","timestamp":"20220817111630","biz_content":"{\"region_code\":\"\",\"user_address\":\"\",\"user_code\":\"fc95d158f8e54fe7ba2e923961440652\"}","sign":"346BEE8C66AC85DC04ED1B9D99A5CD6C"}
返回结果：{"return_code":"SUCCESS","return_msg":"调用成功","result_code":"SUCCESS","result_msg":"申请成功","user_code":"fc95d158f8e54fe7ba2e923961440652","redirect_url":"https://demo.heemoney.com/yunbiz/Account/Register/Index?token=8D0A035F6F76B316206D4C2A89B2B22D5481EC0F51D4555B80D9543F8BBE9CE273C51443635E5944BF12DA761A748F4BF2F5945FD87D944B","is_new_user":"1","sign":"E2D29B34AA02131FB4DA9CB057B7B094"}



签名参数：api_type=1&app_id=hyp200428107197000024987419303A3&biz_content={"region_code":"","user_address":"","user_code":"fc95d158f8e54fe7ba2e923961440652"}&charset=utf-8&method=/v1/LoginWallet&owner_uid=1071972125197&sign_type=MD5&timestamp=20220817112126&version=1.0&key=F8CF6A3E07114934AE684638
签名结果：63DE3DDA34850D5A13049436B5C715C4
请求参数：{"method":"/v1/LoginWallet","version":"1.0","api_type":1,"app_id":"hyp200428107197000024987419303A3","charset":"utf-8","owner_uid":"1071972125197","sign_type":"MD5","timestamp":"20220817112126","biz_content":"{\"region_code\":\"\",\"user_address\":\"\",\"user_code\":\"fc95d158f8e54fe7ba2e923961440652\"}","sign":"63DE3DDA34850D5A13049436B5C715C4"}
返回结果：{"return_code":"SUCCESS","return_msg":"调用成功","result_code":"SUCCESS","result_msg":"申请成功","user_code":"fc95d158f8e54fe7ba2e923961440652","redirect_url":"https://demo.heemoney.com/yunbiz/Confirm/UserLogin?token=5153479BF6F04D66722EAA099816FD5D846970B49E0532BDD1ED6C0F4AAE102F860DF225A7292888","is_new_user":"0","user_uid":"100260317135687","sign":"880CB0879965EB061DFE2C0F8A76361E"}



签名参数：api_type=1&app_id=hyp200428107197000024987419303A3&biz_content={"region_code":"","user_address":"","user_code":"fc95d158f8e54fe7ba2e923961440652"}&charset=utf-8&method=/v1/LoginWallet&owner_uid=1071972125197&sign_type=MD5&timestamp=20220817182356&version=1.0&key=F8CF6A3E07114934AE684638
签名结果：B5AE834AD15FC40D5BFD45F4055D2CD1
请求参数：{"method":"/v1/LoginWallet","version":"1.0","api_type":1,"app_id":"hyp200428107197000024987419303A3","charset":"utf-8","owner_uid":"1071972125197","sign_type":"MD5","timestamp":"20220817182356","biz_content":"{\"region_code\":\"\",\"user_address\":\"\",\"user_code\":\"fc95d158f8e54fe7ba2e923961440652\"}","sign":"B5AE834AD15FC40D5BFD45F4055D2CD1"}
返回结果：{"return_code":"SUCCESS","return_msg":"调用成功","result_code":"SUCCESS","result_msg":"申请成功","user_code":"fc95d158f8e54fe7ba2e923961440652","redirect_url":"https://demo.heemoney.com/yunbiz/Confirm/UserLogin?token=5153479BF6F04D66722EAA099816FD5D846970B49E0532BD37858F182F7D4031EBB20A19D299BFC0","is_new_user":"0","user_uid":"100260317135687","sign":"E0AB791504701399BB4F0678CA30C033"}



查询用户

签名参数：api_type=1&app_id=hyp200428107197000024987419303A3&biz_content={"user_code":"fc95d158f8e5"}&charset=utf-8&method=v1.GetUserInfo&owner_uid=1071972125197&sign_type=MD5&timestamp=20220816183124&version=1.0&key=F8CF6A3E07114934AE684638
签名结果：5ACAFD0FB60FD643736EE56E2EEB2797
请求参数：{"method":"v1.GetUserInfo","version":"1.0","api_type":1,"app_id":"hyp200428107197000024987419303A3","charset":"utf-8","owner_uid":"1071972125197","sign_type":"MD5","timestamp":"20220816183124","biz_content":"{\"user_code\":\"fc95d158f8e5\"}","sign":"5ACAFD0FB60FD643736EE56E2EEB2797"}
返回结果：{"return_code":"SUCCESS","return_msg":"调用成功","result_code":"SUCCESS","result_msg":"获取成功","user_uid":"100260317133667","user_type":"0","user_total_amt_fen":"0","reality_status":"1","bind_card_status":"0","user_name":"张*","user_mobile":"176****4116","user_id_card":"411***********5716","provider_user_id":"5671377","is_set_pay_pwd":"0","reality_grade":"1","sign":"D1661E34917BAFB1E20A7FFE496F636A"}



签名参数：api_type=1&app_id=hyp200428107197000024987419303A3&biz_content={"user_code":"fc95d158f8e54fe7ba2e923961440652"}&charset=utf-8&method=v1.GetUserInfo&owner_uid=1071972125197&sign_type=MD5&timestamp=20220817112349&version=1.0&key=F8CF6A3E07114934AE684638
签名结果：18D7BAC78EBAF4FDA24238FA013250BD
请求参数：{"method":"v1.GetUserInfo","version":"1.0","api_type":1,"app_id":"hyp200428107197000024987419303A3","charset":"utf-8","owner_uid":"1071972125197","sign_type":"MD5","timestamp":"20220817112349","biz_content":"{\"user_code\":\"fc95d158f8e54fe7ba2e923961440652\"}","sign":"18D7BAC78EBAF4FDA24238FA013250BD"}
返回结果：{"return_code":"SUCCESS","return_msg":"调用成功","result_code":"SUCCESS","result_msg":"获取成功","user_uid":"100260317135687","user_type":"0","user_total_amt_fen":"0","reality_status":"1","bind_card_status":"1","user_name":"张*","user_mobile":"176****4116","user_id_card":"411***********5716","provider_user_id":"5671522","is_set_pay_pwd":"1","reality_grade":"1","sign":"12F69B546A9C98DE53F0FF25C1EB04B8"}



申请支付

签名参数：api_type=1&app_id=hyp200428107197000024987419303A3&biz_content={"from_type":"1","out_trade_no":"1","pay_amt_fen":2,"pay_method":2,"return_url":"http://www.baidu.com","user_uid":"100260317133667"}&charset=utf-8&method=v1.ApplyPay&owner_uid=1071972125197&sign_type=MD5&timestamp=20220816183637&version=1.0&key=F8CF6A3E07114934AE684638
签名结果：0907A19E33D404D1E8840D70C52C0A59
请求参数：{"method":"v1.ApplyPay","version":"1.0","api_type":1,"app_id":"hyp200428107197000024987419303A3","charset":"utf-8","owner_uid":"1071972125197","sign_type":"MD5","timestamp":"20220816183637","biz_content":"{\"from_type\":\"1\",\"out_trade_no\":\"1\",\"pay_amt_fen\":2,\"pay_method\":2,\"return_url\":\"http://www.baidu.com\",\"user_uid\":\"100260317133667\"}","sign":"0907A19E33D404D1E8840D70C52C0A59"}
返回结果：{"return_code":"SUCCESS","return_msg":"提交成功","result_code":"SUCCESS","result_msg":"申请成功","out_trade_no":"1","pay_amt_fen":"2","real_amt_fen":"0","redirect_url":"https://demo.heemoney.com/yunbiz/Pay/Cashier/Index?token=2713C5FEC125CB78CC5BFDF8890A538079A8B3BF6D8BF7AD84AE76414CA1A9DA22962FDA860AA706","sign":"B11EE9B9F14049484306C5A7DAADE9BD"}



签名参数：api_type=1&app_id=hyp200428107197000024987419303A3&biz_content={"from_type":"1","out_trade_no":"1","pay_amt_fen":2,"pay_method":2,"return_url":"http://www.baidu.com","user_uid":"100260317135687"}&charset=utf-8&method=v1.ApplyPay&owner_uid=1071972125197&sign_type=MD5&timestamp=20220817112608&version=1.0&key=F8CF6A3E07114934AE684638
签名结果：BC67915C83791EAB955FB68D995D85B8
请求参数：{"method":"v1.ApplyPay","version":"1.0","api_type":1,"app_id":"hyp200428107197000024987419303A3","charset":"utf-8","owner_uid":"1071972125197","sign_type":"MD5","timestamp":"20220817112608","biz_content":"{\"from_type\":\"1\",\"out_trade_no\":\"1\",\"pay_amt_fen\":2,\"pay_method\":2,\"return_url\":\"http://www.baidu.com\",\"user_uid\":\"100260317135687\"}","sign":"BC67915C83791EAB955FB68D995D85B8"}
返回结果：{"return_code":"SUCCESS","return_msg":"提交成功","result_code":"SUCCESS","result_msg":"申请成功","out_trade_no":"1","pay_amt_fen":"2","real_amt_fen":"0","redirect_url":"https://demo.heemoney.com/yunbiz/Pay/Cashier/Index?token=2713C5FEC125CB78722EAA099816FD5D846970B49E0532BDF9275AD355BFC85C44B2D39029669824","sign":"145B3439C9CB8B6324658EA0A0AFD3F6"}



签名参数：api_type=1&app_id=hyp200428107197000024987419303A3&biz_content={"from_type":"1","notify_url":"http://www.baidu.com","out_trade_no":"1","pay_amt_fen":2,"pay_method":2,"return_url":"http://www.baidu.com","user_uid":"100260317135687"}&charset=utf-8&method=v1.ApplyPay&owner_uid=1071972125197&sign_type=MD5&timestamp=20220817144443&version=1.0&key=F8CF6A3E07114934AE684638
签名结果：62C254FA80D84CC27601110798896F21
请求参数：{"method":"v1.ApplyPay","version":"1.0","api_type":1,"app_id":"hyp200428107197000024987419303A3","charset":"utf-8","owner_uid":"1071972125197","sign_type":"MD5","timestamp":"20220817144443","biz_content":"{\"from_type\":\"1\",\"notify_url\":\"http://www.baidu.com\",\"out_trade_no\":\"1\",\"pay_amt_fen\":2,\"pay_method\":2,\"return_url\":\"http://www.baidu.com\",\"user_uid\":\"100260317135687\"}","sign":"62C254FA80D84CC27601110798896F21"}
返回结果：{"return_code":"SUCCESS","return_msg":"提交成功","result_code":"SUCCESS","result_msg":"申请成功","out_trade_no":"1","pay_amt_fen":"2","real_amt_fen":"0","redirect_url":"https://demo.heemoney.com/yunbiz/Pay/Cashier/Index?token=2713C5FEC125CB78722EAA099816FD5D846970B49E0532BD097182FC2084D8A16E2F37FF80989663","sign":"16B264548460A98CAC683587A39D51A6"}









签名参数：api_type=1&app_id=hyp200428107197000024987419303A3&biz_content={"hy_bill_no":"1","notify_url":"http://www.baidu.com","out_share_no":"1","out_trade_no":"1","pay_amt_fen":2,"return_url":"http://www.baidu.com","share_info":"[{\"share_amt_fen\":2,\"user_uid\":\"100260317135687\"}]"}&charset=utf-8&method=v1.ApplyPayShare&owner_uid=1071972125197&sign_type=MD5&timestamp=20220817135427&version=1.0&key=F8CF6A3E07114934AE684638
签名结果：8DEC3E222B6A7091151944417497F971
请求参数：{"method":"v1.ApplyPayShare","version":"1.0","api_type":1,"app_id":"hyp200428107197000024987419303A3","charset":"utf-8","owner_uid":"1071972125197","sign_type":"MD5","timestamp":"20220817135427","biz_content":"{\"hy_bill_no\":\"1\",\"notify_url\":\"http://www.baidu.com\",\"out_share_no\":\"1\",\"out_trade_no\":\"1\",\"pay_amt_fen\":2,\"return_url\":\"http://www.baidu.com\",\"share_info\":\"[{\\\"share_amt_fen\\\":2,\\\"user_uid\\\":\\\"100260317135687\\\"}]\"}","sign":"8DEC3E222B6A7091151944417497F971"}
返回结果：{"return_code":"FAIL","return_msg":"汇付宝支付单号格式错误","sign":"A435080641AADE8EE28358B2B6B56F5E"}





DcPlatformTransferRecords=DcPlatformTransferRecords
 (id=90, direction=0, fromPlatformId=14, toPlatformId=null, fromAddress=null, 
 toAddress=0x0f3af2d363f57ecaf4e74b5f734b202b36ec1fbf, digitalCollectionId=67, taskId=321, status=1, doneAt=null)



 message=
 {"BlockTime":1660719810000,"FuncName":"Transfer","
 Raw":{"transactionHash":"0x9d284200240e6ad00bbb34009d2de32b6713fe22990e4db9af34e326d48dd7c5"},
 "consumerType":"chainListener","Params":{"Form":"0x0","To":"0xf3af2d363f57ecaf4e74b5f734b202b36ec1fbf","TokenId":115}}





签名参数：api_type=1&app_id=hyp200428107197000024987419303A3&biz_content={"hy_bill_no":"H2208180218966AD","notify_url":"http://www.baidu.com","out_share_no":"23","out_trade_no":"23","pay_amt_fen":9,"return_url":"http://www.baidu.com","share_info":"[{\"share_amt_fen\":9,\"user_uid\":\"100260317135687\"}]"}&charset=utf-8&method=v1.ApplyPayShare&owner_uid=1071972125197&sign_type=MD5&timestamp=20220818190144&version=1.0&key=F8CF6A3E07114934AE684638
签名结果：3DD0E45050056842FEEDF339B445315E
请求参数：{"method":"v1.ApplyPayShare","version":"1.0","api_type":1,"app_id":"hyp200428107197000024987419303A3","charset":"utf-8","owner_uid":"1071972125197","sign_type":"MD5","timestamp":"20220818190144","biz_content":"{\"hy_bill_no\":\"H2208180218966AD\",\"notify_url\":\"http://www.baidu.com\",\"out_share_no\":\"23\",\"out_trade_no\":\"23\",\"pay_amt_fen\":9,\"return_url\":\"http://www.baidu.com\",\"share_info\":\"[{\\\"share_amt_fen\\\":9,\\\"user_uid\\\":\\\"100260317135687\\\"}]\"}","sign":"3DD0E45050056842FEEDF339B445315E"}
返回结果：{"return_code":"SUCCESS","return_msg":"提交成功","result_code":"SUCCESS","result_msg":"申请成功","sign":"555697925F4522A296C7C3B819EF53D6"}