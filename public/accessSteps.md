# 接入步骤

## 1.2.1下载DEMO工具包

https://github.com/umpayer/ServiceProviderPlatform

## 1.2.2获取联调配置参数，并调整参数配置

            
|	环境	 |	 参数说明 	|	环境说明 	|
|:--------:|:--------|:--------:|
|联调环境|1、联调环境服务器地址:http://111.205.18.100:8011/entry-provider-plat-client/<br> 2、模拟测试代理商编号编号(acqSpId)：Y471790403<br> 测试商户号(acqMerId)：41509208（交易联调使用此商户号）|1.联调环境不是实际下短信，实际联调请联系开发人员提供短信验证码<br>2.联调环境会在每天上午10：00——10:30，下午5:00——5:30会进行环境更新会存在系统不稳定的情况，请各位知晓<br>3.联调环境微信下午16点后暂时不能交易<br>4.银联二位码需要配合开放平台上测试，路径：https://open.unionpay.com/ajweb/help/qrcodeFormPage|
|生产环境|1、生产环境服务器地址:http://provider.umfintech.com/entry-provider-plat-client/<br>2、生产环境服务商编号(acqSpId)入网后由销售同步Y开头的代理商编号<br>3、入网后请提供接收私钥邮箱给联调人员，并注意查收registration@umpay.com发出的邮件,其中私钥（PXXXXX_公司名.key.XX）用于签名<br>4、入网后请提供接收公钥邮箱给联调人员，并注意查收registration@umpay.com发出的邮件,其中证书（cert_2d59）用于验签|1、商户后台通知地址：切忌后台通知地址为公网地址，且必须确保网络通畅。否则商户将不能收到后台结果通知。|

注意：

开发环境参数和生产环境参数不通用，一定要明确区分两套参数。

返回参数M为必填 O为选填 C为一定条件下必填

## 1.2.3运行DEMO程序
