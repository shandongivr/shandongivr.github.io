# 目录
* [批量订购接口](#批量订购接口)
    * [接口订购](#订购)
    * [接口取消](#取消)
    * [接口查询](#查询)
    * [vac同步](#同步)

***
# 批量订购接口
>接口：**HTTP接口**，请求方式：**GET**，返回值中文编码：**GBK**  
请提供结果**回调地址**  
回调格式：`回调地址URL`?mobile=`计费号码`&order_time=`包月时间`&result=`状态码`&productid=`产品ID`
## 订购
#### 接口说明
接口地址：http://27.221.97.44:6638/ivrbaoyue?phone=`计费号码`&productid=`产品ID`&order_time=`包月时间`
#### 参数说明
**名称**|**属性**|**选项**|**描述**
-------|--------|--------|--------
phone|字符型|必选|计费号码
productid|字符型|必选|产品ID
order_time|字符型|必选|包月时间
#### 返回说明
{"phone":"`计费号码`","productid":"`产品ID`","code":"`状态码`","err_code":"`错误代码`","cause":"`说明`","status_code":"`用户状态码(或没有)`","status_value":"`用户状态说明(或没有)`"}
## 取消
## 查询
## 同步
