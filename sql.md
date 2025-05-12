select top 10 * from ACPTA order by CREATE_DATE desc--TA001
select * from ACPTA  where TA021 like '%飛騰%' --　and CREATOR in ('DS','110001')
select * from ACPTA  where TA021 like '%BPM%' --　and CREATOR in ('DS','110001')
select top 50 * from ACPTA  where CREATOR in ('DS')  order by CREATE_DATE desc
select * from ACPTB  where TB011 like '%飛騰%'
select * from ACPTB  where TB011 like '%HR%'
--SQLServer2016 STD *1 USERCAL*10 (飛騰HR系統使用)
--select top 10 * from ACPTB order by CREATE_DATE desc--TA001

select * from ACPTB  where TB013 like '%飛騰%'
--

select IsPreOrder,IsApproved,* from [order] where id ='UL3D2900000181'
select barcode,orderid,qty,pickupqty,* from [OrderDetail] where orderid ='UL3D2900000181'

select IsPreOrder,statusID,IsLocked,CreatedDt,* from [order] where id ='UL3D2900000181'
--update [order] set IsPreOrder = 0  where id ='UL3D2900000181'


SELECT TrxnBMSDt,TrxnBMSStatus,* FROM [dbo].[SaleReturn] 
WHERE orderid ='MO3D0FE0001539'
TrxnBMSDt=1 *3

MO3D2350001435 居米塞假審驗紀錄