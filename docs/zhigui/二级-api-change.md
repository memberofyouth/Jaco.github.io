````
接口路径，及请求方式修改：

授权回调： /personal-center/users/approve_callback  请求类型不变路径修改为 /personal-center/users/approval-callback

获取授权码： /personal-center/users/gain_auth_code   请求类型不变路径修改为 /personal-center/users/auth-codes

解除授权： /personal-center/users/cancel_authorization   请求类型修改为 delete 路径修改为  /personal-center/users/authorizations


发送验证码接口
改了到system服务里 ，参数加了个短信类型，参考api  https://api-doc.zhigui.com/project/558/interface/api/18301

````



泽群userId： 838b626e-7af1-4e11-8edd-08c3337f7176



自我管理

```
SELECT
 dc.meta_name,o.*
FROM orders o left join digital_collections dc on dc.id = o.digital_collection_id  where o.buyer_id = '72db6467-7115-481c-89f9-c966516a9ac5' and o.created_at >= '2022-10-26' order by o.created_at desc



SELECT
 aes_decrypt(from_base64(u.id_card_name), 'a4e97ea51a347077f6588cca8f1fc406'),count(1),dc.meta_name,o.total_amount
FROM orders o left join digital_collections dc on dc.id = o.digital_collection_id left join users u on u.id = buyer_id  where dc.platform_id = 26 and o.created_at >= '2022-11-16' and o.status = 1 group by buyer_id order by o.created_at desc



转账查询：


select p.payment_platform_user_id,aes_decrypt(from_base64(du.phone), 'a4e97ea51a347077f6588cca8f1fc406') phone from payment_platform_accounts p inner join (SELECT
  *
FROM users where aes_decrypt(from_base64(phone), 'a4e97ea51a347077f6588cca8f1fc406') in ('13025151563',
                '13472062385',
                '13831475262',
                '13983842653',
                '15187014784',
                '15315919273',
                '15588701080',
                '15602348042',
                '15659199850',
                '15731489122',
                '18279112381',
                '18389699361',
                '18567259316',
                '18583101797',
                '18738740301',
                '18741817882',
                '18820291520',
                '18856713191',
                '18867790590',
                '18953307257')) du on p.user_id = du.id where p.platform_id = 1


```



```
待签名报文：Fo2d4x7+Kk3mI0Abzojcy3ZOSslZYtoNLYr0vANiHsfPLjif/0LeqXEkeELBzzHXrY28oMYNYuORvlxV8Taf0tmMDQMWn49hzJMslVyHf7O+0ktpb/3+VFAq9nTjS1x5GmXjFc9gn6KxMdqyiSwItw==
请求方法：electrans/ceas.elec.trans.info.query
 请求报文：{"data":"Fo2d4x7+Kk3mI0Abzojcy3ZOSslZYtoNLYr0vANiHsfPLjif/0LeqXEkeELBzzHXrY28oMYNYuORvlxV8Taf0tmMDQMWn49hzJMslVyHf7O+0ktpb/3+VFAq9nTjS1x5GmXjFc9gn6KxMdqyiSwItw==","sign":"Q9rpElo7JnpAPJ419ybnhJ/pbgAnF1YGsg1K6x90GGMNYVDFF0ywvut5h6AHjcApbkPUEIPD13RY3DZLJiC1XckOlnKO4SbTMzV0garXt8pnjGb6il1WFwFBX5Ez5t5upOcbe0+Sij5bDwCglfHz2ZGpCPROiTEopZPrxD3GjwtV7JSlT0SDpYHECbPvFNfEUi5tzyq66Xpv1ZF2vcQJSJAzL0ry+uwKMLargllRzQGB67VLxipjuw7IBv+jKPYGg3jGf1HkuEzN9n9pGuoxcArfcR3zc25E4UVyJgpZlz4bKtUPE4GqZB+uHIsNqfUzPFr5CgwFPh+CMiO4C8Uh4w==","mid":"6888801116904","signType":"SHA1WithRSA","encryptKey":"TcOB8XoKQAYc2WJyYjxqqq4KPr/5HjLmLWDU/aEUpztaZiMWXJ0hsQlP9foSQu51QWcKR4+unWJ8hItoyICP5UTAz5JkUYqeTH6eb4SiW68il3iueEWK2TQ6vhhYG9s0iS5wFgNKJxUC3L+NSoG5KfDZ6cJ2//C37Bxsg6d0OIKiE1W96puQ3wznwS6pmSwO11lpacBE4+fboJHkY++OHC+QZnLMY00uN37GhhJv5AP54JO6yq/Cr7rnsqAkTqDTJXodDy7IO2uHAbx+cgFmQ/K48Wj/6e4G+DhJ7QCF6IhymW5qES3nw0UJwVV5MFgcbfqnWHYHRnqn3dNuRyXgFQ==","customerOrderNo":"f8a819796eed387e78abc3b83d463311","encryptType":"AES"}
 响应报文：{"data":"jBCDazTL35nQDMzqm8GHGoQmW7VFj/0crAzkNKqfYE8xutZUgHH6f7jGNFmWFQNvbevY/8Ob1s2rzWdFhdVhk+5iGoXGTzXFVjU1cDbgctWU243q6XehdDIk8Fs7l08NlhOR9Cbv8uOFch3ht3MPxZGpmUWgYxoyo9QYGNA9ZrCwIu/RkGT2rGpyFoaZ1ovmgZMStHUXHdXpHghwp62LwDkxbJlmvDsxKa7Bcnp3wqqLaHp7lsGvDwKfEDD0RG0ifljngJMNO9d4j/ILLgHqOLlB8YisK2HuRaCAZC94QekXAX0WZt069vUxVlM1d87h6uqxa5OvqYZRF0PPAo1gUg==","response":{"responseDesc":"报文解密失败","responseTime":"20221123221717","mid":"6888801116904","sandSerialNo":"CEAS2022112322171725492753","responseStatus":"01","customerOrderNo":"f8a819796eed387e78abc3b83d463311","version":"1.0.0","responseCode":"03005"},"sign":"phEnput/qCREEcdUppHVNSoYQAnssp4tnHp2ytcxsdnOzwdcjAVmytPAAflXMVypyCc/DFsm4QgmNrHNuoT+YS6XRvVOdRHufnjIIIl/EiZJc9mLnfvsbB9vP+ycJSvgjsuXJeeNLN92N37v9yGcnFQPBioEPXiTLcUB+qNCEpv094vhdqD/5ihFQ5Nk8KSj0mV8pHnGR2W8RthJi7/SEet8Ur5aazxBg/0/GKcLLLM59TJEzlub4f3GV11ueRMGUnMfEBlSr9D2OM5DREQWVbty1fw9h/3yxUleA2+sEifuckr5uCAEhRN5DlPiomsoBNcZVQfOx4lFWO49OzIQxg==","signType":"SHA1WithRSA","encryptKey":"oWZg/Vq3gsFtaEl+D1XhM3FtfK1LX7BM6VQMb8aBm24thw20FW+1WHpuzGXOBmGaVJQuYitNJ2X8wHz0uyHwqkAgYIAZo6XNTsJ5bf1dP/UQE8aWUBqPRRC9lGwH8rdBkgb1NJgnEihW07vjPKC+REN5zVdbkALlt5OKpwYgJlZRxmcxawfQG9nadjrLY3/rE9nDHPd116Y+hqNC73hI1td0mbIKd2j66vjGaSAmorAYEy8/H2ozV/ot2T2KGQRFkpu/giXrtEVWgH+RtYSJwQl796j/+TGszpTuxDvaza4LmmflWgr2uKr6PP36AGcHFS7oNmmCkdlR5unjMk3UAw==","encryptType":"AES"}
 签名验证失败
 
 
钱包支付签名后参数 ----->>>>>> 0122E98620C1F1A6021FA1B92F6A0D40
钱包支付签名参数 ----->>>>>> app_id=hyp2208171243760001955850C9A2350&bill_status=Success&hy_bill_no=H2302273377796AS&notify_type=Trade&out_trade_no=62b3cd4b159d64e22f91581e80e8d7791&owner_uid=1243762139077&pay_amt_fen=&pay_method=&pay_option=&real_amt_fen=11&time_end=20230227175501&version=2&key=7FC7418575044F5CB01FD644
签名后参数 ----->>>>>> E6301A586CEB7D1B9FE41C0B912A39CF
签名参数 ----->>>>>> app_id=hyp2208171243760001955850C9A2350&bill_status=Success&hy_bill_no=H2302273377796AS&notify_type=Trade&out_trade_no=62b3cd4b159d64e22f91581e80e8d7791&owner_uid=1243762139077&pay_amt_fen=&pay_method=&real_amt_fen=11&time_end=20230227175501&version=2&key=7FC7418575044F5CB01FD644
```

