```sql
-- 根据藏品id 查询 平台转移记录
SELECT
  *
FROM dc_platform_transfer_records where digital_collection_id = '2121'

-- 查询所有group
SELECT
  dcg.id,dcg.platform_id,dcg.name,dcg.description_file_url
FROM digital_collection_group dcg where deleted = 0


--查询藏品 group 及其明细

SELECT
  dcg.id,dcg.platform_id,dcg.name,dcg.description_file_url,dcga.id dcgaId,dcga.value,dcga.attribute_key_id,dcga.value_description
FROM digital_collection_group dcg LEFT JOIN digital_collection_group_attributes dcga on dcg.id = dcga.digital_collection_group_id where dcg.deleted = 0


select * from digital_collection_group where platform_raw_id = '300009784'
-- 查询group为：12 的交易订单 包括稀有度

SELECT
  o.total_amount,o.handling_fee,o.income_amount,o.bill_no,o.created_at orderTime,dc.*
FROM orders o left join digital_collections dc on o.digital_collection_id = dc.id  where o.digital_collection_id in (SELECT
  id
FROM digital_collections where group_id = 12) and o.status = 1 and dc.meta_attributes like '%史诗%' order by o.total_amount asc


-- 查询藏品限价

SELECT
  dcg.name,lr.valid_date,lr.min_limit_price,lr.max_limit_price
FROM listing_rule lr, digital_collection_group dcg where lr.digital_collection_group_id = dcg.id group by digital_collection_group_id order by lr.valid_date desc


-- 未收书续费订单
SELECT
  dc.meta_name,o.total_amount,o.handling_fee,o.income_amount,o.bill_no,o.created_at orderTime
FROM orders o left join digital_collections dc on o.digital_collection_id = dc.id  where o.status = 1 and handling_fee = 0.00 order by o.created_at desc


SET block_encryption_mode = 'aes-256-ecb';
aes_decrypt(from_base64(phone), 'a4e97ea51a347077f6588cca8f1fc406') = '18690739777'


-- 查询手机号

select * from users where  aes_decrypt(from_base64(phone), 'a4e97ea51a347077f6588cca8f1fc406') = '13210156370'

```













