# 项目介绍
## 前言
#### jsdelivr 项目是2021年12月20日下午因为一些原因jsdelivr已经失去了国内的IPC备案那么导致了 网宿关闭了jsdelivr的 的国内加速 然后切换了 Fastly 在jsDelivr被吊销ICP许可证四个月后的4月28日开始被DNS污染，导致国内访问解析更加困难 和我的ayaoblog.com的一样情况 都是被污染了 ，我是被动了 我是因为yaoblog.COM被污染导致我连坐，现在jsdelivr的情况好不少，但是没有国内节点还是有点慢....
### 项目概述
在2021年12月21晚上上线的 jsd.eagleyao.com Version 1.0 使用了三台香港LH配合加速

一直到 2022-09-26 jsd.cdn.zzko.cn 新域名备案下来 Version 2.0  使用了三台香港LH加1孟买配合加速

由于访问cdn.jsdelivr.net会301跳www.jsdelivr.com 同理jsd.cdn.zzko.cn也会301跳www.jsdelivr.com  我设置了访问301转200了 cdn源在用户这边不进行跳转直接进行展示 也就是伪200 
![image](https://user-images.githubusercontent.com/86733666/194760732-5c91dd9a-70c9-4ec5-874a-c844732009c7.png)
比如说
https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/
直接改成
https://jsd.cdn.zzko.cn/npm/font-awesome@4.7.0/

换域名主要是com年年涨价，也受到美元汇率影响导致注册商涨价 也想短点好


目前使用Version 3.0加速 使用 SNI +hosts 方式加速 (已实现) 2022 年 10 月 6 日 目前全面升级完成 哈哈 使用了腾讯云香港 32 个 ip 以后会更多的 所有域名都所有了这个配置，欢迎大家来使用


CDN 侧配置

![image](https://user-images.githubusercontent.com/86733666/194452743-5af3b216-ac40-4bd5-bd56-6453814b11b6.png)

不要闲着去攻击源 不然我真的会栓 Q 的 还有好几个是 30Mpbs 的服务器 宽带太小没有加 这些都是在 100Mpbs 以上的的 IP。。。。后期可能加上）

www.itdog.cn  测试情况

有缓存的情况下

![image](https://user-images.githubusercontent.com/86733666/194452812-bff30e13-ac87-4d6e-8b88-fb599a28bc11.png)

关闭缓存的情况下

![image](https://user-images.githubusercontent.com/86733666/194452840-76775bb3-e7c9-4db6-86a6-d67e98c6fa4a.png)

整体来说性能无差异，但是考虑到正常情况下还是增加了一定缓存

官方给我展示的被攻击日志 

![image](https://user-images.githubusercontent.com/86733666/194457040-e599e47d-acbf-454f-b405-e12304e762d2.png)

一些请求头问题介绍

![image](https://user-images.githubusercontent.com/86733666/194452924-1334eb1f-f468-4b89-aa76-97bf8900fc33.png)

在请求头中

ayao: https://www.ayao.ltd

是我的个人主页 想让知道这个负责人的网站

china-jsdelivr: The jsdelivr mirror station is a public CDN acceleration plan for . It has an effective ICP filing application permit issued by the Chinese government, use Tencent Cloud CDN to provide domestic accelerated services  I believe you can see this sentence. I hope you don't attack the website, personal website maintenance funds are limited The good Internet atmosphere is inseparable from everyones joint efforts.

大体意思就是说
jsdelivr镜像是的公共CDN加速计划。 它具有中国政府颁发的有效的ICP申请许可，使用Tencent Cloud CDN提供国内加速服务，我相信您可以看到这句话。 我希望您不要攻击网站，个人网站维护资金有限，良好的互联网氛围与每个人的共同努力都不分开。

（google机翻）




是项目介绍 介绍了这个项目的具体原因。

contact: admin@eebbk.top

是管理员邮箱 任何问题可以发邮件。

static-resources: https://www.zzko.cn

是静态域名专属域名

server: ayao

copyright: ayao

维护人标示

![image](https://user-images.githubusercontent.com/86733666/194453609-37f68ed7-2347-4078-b951-f9eafe7326c5.png)

速度测试
还是不错的


不要去CC我 目前没有过多限制请求 每秒单ip是500Qps 我也相信不会触碰到某些人利益吧。。。公益行为 我也希望灰黑产业的大佬别搞我把静态资源随便引用到自己违法违规站点！，就相当于我为违法违规站提供服务，您搞违法的事情，就不要带上我了谢谢，大家都是中国人，中国人别为难中国人，谢谢


## 项目支持
### 我们使用的服务
<a href="https://cloud.tencent.com" id="Qcloud" target="_blank"><img src="https://user-images.githubusercontent.com/86733666/194760853-f5e77e56-92aa-4d2f-9c1e-3a1e61c124bc.png" width="200" height="55"></a>
<a href="https://www.azure.cn" id="Qcloud" target="_blank"><img src="https://user-images.githubusercontent.com/86733666/194761263-fe1522ce-3933-4a8b-bc52-09e4fad482e9.png" width="230" height="50"></a>

### 感谢以下实质性加速赞助
<a href="https://cloud.tencent.com" id="Qcloud" target="_blank"><img src="https://user-images.githubusercontent.com/86733666/194760853-f5e77e56-92aa-4d2f-9c1e-3a1e61c124bc.png" width="200" height="55"></a>
<a href="https://www.xgzwlkjltd.com/" id="Qcloud" target="_blank"><img src="https://user-images.githubusercontent.com/86733666/194762270-887fc7e3-db41-40d7-b13c-46dde45534ec.png"></a>


### 赞助详情情况
<div class="md-typeset__scrollwrap"><div class="md-typeset__table"><table>
<thead>
<tr>
<th align="center">序号</th>
<th align="center">昵称/网站</th>
<th align="center">日期</th>
<th align="center">捐赠方式</th>
<th align="center">金额</th>
  <th align="center">留言/备注</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center">1</td>
<td align="center">腾讯云</td>
<td align="center">2021/12-长期</td>
<td align="center">源站和CDN</td>
<td align="center">-</td>
  <td align="center">无</td>
</tr>
<tr>
<td align="center">2</td>
<td align="center">合肥市小桂子网络科技有限公司</td>
<td align="center">2022/10-09-长期</td>
<td align="center">CDN</td>
<td align="center">-</td>
  <td align="center">无</td>
</tr>
</tbody>
</table></div></div>
