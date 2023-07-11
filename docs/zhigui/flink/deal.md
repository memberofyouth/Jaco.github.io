

```
1、删除es索引，curl -XDELETE  http://xxx:9200/fm_hot_group_list

2、update fm_hot_group_list set deleted =5 where deleted =0;
3、启动flink job

4、update fm_hot_group_list set deleted =0 where deleted =5;




Join(joinType=[LeftOuterJoin], where=[(self_group_id = group_id)], select=[group_id, market_min_price, sequence, updated_at, query_at, id0, name, kept_img_url, name0, sellAmount1, price, id3, total_amount, payment_at, self_group_id], leftInputSpec=[NoUniqueKey], rightInputSpec=[NoUniqueKey]) -> Calc(select=[id0 AS id, name AS groupName, sequence, id3 AS goodsId, name0 AS platformName, kept_img_url AS imgUrl, IFNULL(price, 0:DOUBLE) AS minPrice, IFNULL(market_min_price, 0:DOUBLE) AS marketMinPrice, IFNULL(sellAmount1, 0:BIGINT) AS currentSellCount, IFNULL(total_amount, 0:DOUBLE) AS orderPrice, payment_at AS paymentAt, updated_at AS updatedAt, query_at AS queryAt]) -> NotNullEnforcer(fields=[id])



```

