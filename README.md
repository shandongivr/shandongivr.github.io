# 目录
* [通知](#通知)
* [批量订购接口](#批量订购接口)
    * [接口订购](#订购)
    * [接口取消](#取消)
    * [接口查询](#查询)
    * [vac同步](#同步)  

***
## 通知
***
## 批量订购接口
>接口：**HTTP接口**，请求方式：**GET**，返回值中文编码：**GBK**  
请提供结果**回调地址**  
回调格式：`回调地址URL`?mobile=`计费号码`&order_time=`包月时间`&result=[`状态码`](#回调状态码)&productid=`产品ID`

---
### 订购
#### 接口说明
>接口地址：**http:**//27.221.97.44:6638/ivrbaoyue?phone=`计费号码`&productid=`产品ID`&order_time=`包月时间`

#### 参数说明
<table>
   <tr>
      <th>名称</th><th>属性</th><th>选项</th><th>描述</th>
   </tr>
   <tr>
      <td>phone</td><td>字符型</td><td>必选</td><td>计费号码</td>
   </tr>
   <tr>
      <td>productid</td><td>字符型</td><td>必选</td><td>产品ID</td>
   </tr>
   <tr>
      <td>order_time</td><td>字符型</td><td>必选</td><td>包月时间</td>
   </tr>
</table>  

#### 返回说明
>{"phone":"`计费号码`","productid":"`产品ID`","code":"`状态码`","err_code":"`错误代码`","cause":"`说明`","status_code":"`用户状态码(或没有)`","status_value":"`用户状态说明(或没有)`"}

---
### 取消
#### 接口说明
>接口地址：**http:**//27.221.97.44:6638/ivrquxiao?phone=`计费号码`&productid=`产品ID`&order_time=`包月时间`

#### 参数说明
<table>
   <tr>
      <th>名称</th><th>属性</th><th>选项</th><th>描述</th>
   </tr>
   <tr>
      <td>phone</td><td>字符型</td><td>必选</td><td>计费号码</td>
   </tr>
   <tr>
      <td>productid</td><td>字符型</td><td>必选</td><td>产品ID</td>
   </tr>
   <tr>
      <td>order_time</td><td>字符型</td><td>必选</td><td>包月时间</td>
   </tr>
</table>  

#### 返回说明
>{"phone":"`计费号码`","productid":"`产品ID`","code":"`状态码`","err_code":"`错误代码`","cause":"`说明`","status_code":"`用户状态码(或没有)`","status_value":"`用户状态说明(或没有)`"}

---
### 查询
#### 接口说明
>接口地址：**http:**//27.221.97.44:6638/ivrchaxun?phone=`计费号码`&productid=`产品ID`

#### 参数说明
<table>
   <tr>
      <th>名称</th><th>属性</th><th>选项</th><th>描述</th>
   </tr>
   <tr>
      <td>phone</td><td>字符型</td><td>必选</td><td>计费号码</td>
   </tr>
   <tr>
      <td>productid</td><td>字符型</td><td>必选</td><td>产品ID</td>
   </tr>
</table>  

#### 返回说明
>{"phone":"`计费号码`","productid":"`产品ID`","code":"`状态码`","err_code":"`错误代码`","cause":"`说明`","status_code":"`用户状态码(或没有)`","status_value":"`用户状态说明(或没有)`"}

***
### 同步
>Prm上：合作伙伴订购url **http**://27.221.97.48:8837  
prm改产品属性：订购或点播关系是否通知sp，要改为通知  
同步信息通过回调地址返回 回调[result](#回调状态码)为`2`

***
### 回调状态码
>result为0代表订购成功，为1代表订购失败，2代表联通营业系统订购或取消成功
