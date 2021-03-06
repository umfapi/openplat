# 刷卡支付-用户分账查询
**简要描述：**
- 分账状态查询

**请求URL：** 
- 商户->联动优势
`{交易服务根地址}/pay/ledgerAccountQuery`

**请求方式：**
- POST 

**请求参数：** 

|	字段	|	名称	|	长度	|	必填	|   说明|
|:--------:|:--------:|:--------:|:--------:|:--------|
|	acqSpId	|	代理商编号	|	10	|	M	|	代理商编号(联动平台分配)	|
|	acqMerId	|	商户号	|	8	|	M	|	商户号(联动平台分配)	|
|	orderNo	|	商户订单号	|	64	|	M	|	商户的支付订单号	|
|	ledgerOrderNo	|	分账订单号	|	64	|	M	|	商户的分账支付订单号	|
|	signature	|	签名	|	256	|	M	|参见签名机制	|	|



 **返回参数说明** 
 
|	字段	|	名称	|	长度	|	必填	|	说明	|
|--------|-------|--------|--------|--------|
|	respCode	|	返回码	|	8	|	M	|	返回码	|
|	respMsg	|	返回信息	|	128	|	M	|	返回信息	|
|	resultCode	|	分账结果码	|	8	|	O	|	返回码	|
|	resultMsg	|	分账结果信息	|	128	|	O	|	返回信息	|
|	platDate	|	平台日期	|	16	|	O	|	平台日期   |
|	orderNo	|	商户订单号	|	64	|	O	|		|
|	ledgerOrderNo	|	分账订单号	|	64	|	O	|	商户的分账支付订单号	|
|	transLedgerOrderNo	|	联动分账订单号	|	32	|	O	|	联动优势的订单号|
|	ledgerResult	|	分账结果信息	|	1024	|	O	|		|
|	signature	|	签名	|	256	|	M	|	参见签名机制	|
|	|
|	ledgerResult格式如下：		|
|	字段	 |	名称	  |	长度  	|	必填  	|	说明	  |
|	ledgerTrans	|	分账流水号	|	64	|	O	|	商户的分账流水号	|
|	ledgerAcqMerId    	|	分账商户号	|	13	|	O	|		|
|	ledgerTxnAmt	|	分账金额	|	13	|	O	|	单位:分	|
|	ledgerMerPriv	|	分账商户私有域	|	128	|	O	|	商户私有域	|
|	isTrueTime	|	是否实时到账	|	128	|	O	|	0:是 1:否	|
