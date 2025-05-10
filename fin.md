--select * from COPTG where TG001 = N'2301'  AND (COPTG.TG002 = N'25040800066')
select TH004,TH005,TH006,TH008,* from COPTH where TH001 = N'2301'  AND (COPTH.TH002 = N'25040800066')
--select * from COPTI where TI001 = N'2401'  AND (COPTI.TI002 = N'25041500002')
select TJ004,TJ005,TJ006,TJ007,* from COPTJ where TJ001 = N'2401'  AND (COPTJ.TJ002 = N'25041500002')
--select * from COPTG where TG001 = N'2301'  AND (COPTG.TG002 = N'25041500001')
select TH004,TH005,TH006,TH008,* from COPTH where TH001 = N'2301'  AND (COPTH.TH002 = N'25041500001')




--select MB001,MB002,MB003 from INVMB where MB001 ='G000000151013'
----查詢特定品號在特定倉別庫存數大於零的庫存數
select  top 100 substring (C.MC001,1,13) as 商品編號,
--rtrim(C.MC001) as 商品編號,
B.MB002 as 商品名稱,
B.MB003 as 規格,
C.MC007 as 庫存數量,
rtrim(C.MC002) as 庫別,
M.MC002 as 庫名
--MB006 as 品牌
from Goodwow.dbo.INVMC C 
inner join INVMB B on C.MC001=B.MB001
inner join CMSMC M on C.MC002=M.MC001
where 
--C.MC002 like '%URL21%' and ----指定倉別
-- URL21 3096
C.MC007 <> 0 and  ---- 庫存>0
C.MC001 in(
'H400032271903'
)
--好好喔，外倉出貨，客人退貨，美環還打退貨單造成ERP負庫存