清理缓存接口上线了参考 目前是Test 阶段 后续需要扣除你在站点签到或者是活动的积分
https://www.cuteapi.com/?CuteAPI=doc&id=15
https://www.cuteapi.cn/?CuteAPI=doc&id=15

图片不支持的！！！


ACG请先像管理员申请加白在加速！！！！
![image](https://github.com/54ayao/JSDMirror/assets/86733666/be71ccff-b570-4fd4-b50d-581db10a34aa)
怎么玩受不了啊！！！



反馈渠道
微信>>企业微信>企业微信邮件>tg>QQ>bilibili

可能出现解封的机会

![image](https://github.com/54ayao/EdgeJSedSpeed/assets/86733666/d80c0729-8d4c-4107-96fa-0ef8332bc99b)

如果出现这个情况请联系管理员进行处理


![image](https://github.com/54ayao/EdgeJSedSpeed/assets/86733666/54c1303f-a229-498f-9774-3f7879a0c134)
![image](https://github.com/54ayao/EdgeJSedSpeed/assets/86733666/3c61c25d-bc02-4dbe-a319-193ad2591501)
如果出现这个情况请联系管理员进行询问是什么违规


可以解封情况
![image](https://github.com/54ayao/EdgeJSedSpeed/assets/86733666/dab0af03-2670-4c23-8a57-eb384ddc3c29)

说明：

1.平台发现部分人使用多个//绕过封禁系统，达到继续使用的目的 ，在这里我们联系CDN供应商特殊配置修复了使用多个//绕过封禁系统的BUG（目录侧输入大于等于俩个/ 系统按一个计算）

2.可以申请不审核 但是仅限于ACG、正常图片、博客标记、日常生活 等等 需要有一定的信誉累计

(被审核系统处理了一定要跟我说 我第一时间处理！！！)
（2024 3月现在被封的都可以申请解封）
## 什么是  EdgeJSedSpeed ？（基于某些考虑改名了）
EdgeJSedSpeed
本项目于 2021 年 12 月 21 上线 在此期间我们也在不断的测试和迭代 从最开始的直接镜像到服务器再到使用云函数等更新来提高成功率和速度 
最开始我们开始直接在CDN反向代理jsDelivr官方但是动不动链接失败 ，后来查询一下日志是被污染了 CDN在切换源站上浪费了时间，后来我们使用了腾讯云香港LH反向代理，但是，受限于30MBbs的宽带导致速度平平无奇，在后来尝试使用云函数加速，也问了一下jsDelivr没有完全被国内禁止使用 云函数镜像jsDelivr 不属于跨境访问
当然你“认为”我们镜像jsDelivr是为了窃取jsDelivr官方流量那没有使用的必要的哈 出发点都是错误了 你所有的请求都是毫无保留且不增加任何修改转发给jsDelivr 即使修改了首页 增加了广告其实也是对您使用不会产生本质上的影响，还是不明白的话，那么你可以选择自建或者是使用COS或者是OSS回源jsDelivr来进行加速

JSDelivr 镜像站 分发工作原理
业务源站域名为 jsd.cdn.zzko.cn，域名接入 CDN 加速服务后，当您发起 HTTP 请求时，会先发起DNS解析请求获取最优的访问IP，之后再向获取的访问IP发起内容请求，实际请求完整过程如下：
![image](https://github.com/54ayao/EdgeJSedSpeed/assets/86733666/01d6eaba-4957-4d94-be88-498455e30ef6)

## JSDelivr 镜像站 分发工作原理

1.用户在网站或APP请求 jsd.cdn.zzko.cn 下的某资源（如/gh/54ayao/EdgeJSedSpeed@blob/main/static/8dd0ee58-44cd-4bce-b470-3d581129e30f.png，index.php，/gh/54ayao/EdgeJSedSpeed@edit/main/README.md )，会先向本地DNS发起域名解析请求。

2.本地DNS检查缓存中是否有jsd.cdn.zzko.cn的IP地址记录：如果有缓存则直接返回给终端用户，若没有缓存则向授权DNS查询jsd.cdn.zzko.cn解析。

3.授权DNS服务器解析jsd.cdn.zzko.cn，假如发现域名已经解析到了CNAME：jsd.cdn.zzko.cn.cdn.fusioncdn.cn，并响应给本地服务器。

4.本地服务器发起jsd.cdn.zzko.cn.cdn.fusioncdn.cn解析请求，并直接返回a记录不再返回多余的cname,当前镜像站请求被指向白山CDN全球智能调度系统。

5.CDN智能调度系统对域名进行智能解析，将离用户最近的响应速度最快的CDN节点IP地址返回给本地DNS。

6.用户获取响应速度最快的CDN节点IP地址。

7.用户网站或APP在得到最佳节点的IP地址以后，向CDN边缘节点发出访问请求。

8.如果该边缘节点IP服务器已有缓存该资源，节点将数据直接返回给用户（如12），若无缓存则向白山中间源请求内容。

9.若中间源服务器已有缓存该资源，节点将数据直接返回给边缘节点（如11），若无缓存由CDN判断文件路径/后缀 选择对应负责的源服务器去请求上游内容。

9.1 当用户访问非jsdelivr加速项目的时候CDN系统回源腾讯云轻量应用服务器加载镜像站前端，并且缓存部分资源

9.2 当用户访问jsdelivr加速项目的时候CDN系统判断非图片/视频格式回源香港云函数，若有缓存则向白山中间源提供资源，若无缓存则向云函数服务器请求内容，当云函数确认没有缓存则触发9.2.1回官方拉取资源。

9.3 当用户访问jsdelivr加速项目的时候CDN系统判断图片/视频格式回源香港COS， 若有资源则向白山中间源提供资源并要求缓存，若cos内无当前则白山中间源向香港cos服务器请求内容，当香港cos确认没有当前文件则触发9.3.1回广州COS拉取资源，广州cos如果确认有当前资源则向香港cos提供相关资源，反之没有的话我们会尝试去国际站镜像站拉相关资源，为避免拉取过程中导致资源异常我们302，在如果广州cos如果确认没有，触发9.3.2向让广州轻量帮忙进行URL转码 ，触发9.3.3获取资源，进行9.3.5操作 然后广州轻量向广州COS发送数据，由广州COS审核内容 审核通过则设置200状态码，审核不通过则设置400状态码，文件被冻结，用户再次访问的时候，香港cos确认没有没有该资源则触发9.3.6回广州COS拉取资源并且再次审核 ， 只有文件正常状态下才能正常获取，也就是非冻结状态，也就是审核通过的，香港也是有审核的，如果复审审核不通过则设置400状态码文件被冻结，当用户第3次访问状态码为200的资源可以正常加载，400状态码的需要找管理员审核解封，也就是说你必须要过两次审核才能正常加载，后续等于稳定运营之后只用审核一次

（图片整个过程约1分钟，视频根据大小决定）

10.根据不同内容源站组在向白山中间源返回数据。

11.白山中间源获取响应内容，并缓存数据，同时将内容响应给边缘节点。

12.边缘节点获取数据，并缓存，同时将内容响应给用户。

# 简介

EdgeJSedSpeed  是一个免费依托于国内CDN（内容交付网络）。以及云函数等产品对上游jsdelivr官方的资源进行更新及转发，我们与jsdelivr官方的Github和NPM还有WP都可以甚至是combine 紧密集成，也是希望大家可以给自己的网站能够自动静态文件/音视频文件获得一定的加速，当然我们使用的初衷是让所有开源项目提供可靠的CDN服务，但是也可以用于私有化场景，博客，论坛，等等，当然依托于国内大厂提供稳定的 CDN，可用于具有大量流量的流行网站上的生产。<del>没有带宽限制</del>保证正常情况下合理的速度或高级功能，任何人都可以完全免费使用，但是这个对于我们来说EdgeJSedSpeed在流量方面也是要做好预估的，但是EdgeJSedSpeed是一个不好说的一个项目，这里的突发流量还是比较多的，我们目前在云厂流量是800GB-1000GB 一个月左右，为了产生不必要的回源请求，降低源的流量流出，我们会比jsdelivr官方缓存可能高达1倍左右。我们以后在这里也会开放出api来让用户来清理缓存,虽然说由于EdgeJSedSpeed不像jsDelivr是一个依托于jsDelivr赞助商支持的免费的CDN项目相反EdgeJSedSpeed我们所有流量都是我们来承担。，之前考虑过使用多家CDN进行拉平处理来平均进行流量调度以获得更好的性能，但它也使我们能够避免单个 CDN 过载。但是多家CDN可能面临一些问题 比如说 账单分散 缓存过多 对于云函数服务器压力过大，反而会产生更多的费用，或者说某个CDN欠费导致局部故障，这些我们都在想办法解决，
我们的主要费用包括就是CDN流量以及HTTPS请求费，图片审核费用，如果有能力的用户可以选择赞助CDN以及Money 当然更好了，我们会在子页面公式内容以及去向 可以参考最下面的赞助，

我们境内使用了 <del>阿里</del>、<del>腾讯</del>、<del>百度</del>、<del>华为</del>、<del>网宿</del>、<del>金山</del>，白山
海外使用了cloudflare、<del>CDNetWorks</del>、<del>Tencent Cloud</del>、bunny、 Vercel  进行分发
划线的是系统目前暂时停止对其cdn节点停止调度 




## 使用教程
参考下列首页   

境内站 https://jsd.cdn.zzko.cn/  
![image](https://github.com/54ayao/EdgeJSedSpeed/assets/86733666/41a36d00-0584-4d9e-9896-758d4b9c937f)


国际站 https://cdn.jsdelivr.us/  
![image](https://github.com/54ayao/EdgeJSedSpeed/assets/86733666/0d3ceee8-94b3-4415-97ca-fb9511e9a7d2)


根据有关部门要求，我们对平台协议进行了更新。

## 遵守平台规定
根据中华人民共和国工业和信息化部、公安部等部委关于加强在公共信息服务中传播信息管理的有关规定和相关精神，要求各单位落实完毕

一、不利用像站危害国家安全、泄露国家秘密，不侵犯国家的、社会的、集体的利益和第三方的合法权益，不从事违法犯罪活动、妨碍社会治安的活动。

1.煽动抗拒、破坏宪法和法律、行政法规实施的；

2.煽动颠覆国家主权，推翻社会主义制度的；

3.煽动分裂国家、破坏国家统一的;

4.煽动民族仇恨、民族歧视，破坏民族团结的；

5.捏造或者歪曲事实，散布谣言，扰乱社会秩序的；

6.宣传封建迷信、淫秽、色情、赌博、暴力、凶杀、恐怖犯罪的；

7.公然侮辱他人或者捏造事实诽谤他人的；

8.损害国家机关信誉的;

9.传播不实信息，危害或对社会安全行为造成恐慌

10.其它违反宪法和法律、行政法规的。

二、色情低俗类

1.表现或隐晦表现性行为、令人产生性联想、具有挑逗性或者污辱性的内容；

2.对人体性部位的直接暴露和描写；

3.对性行为、性过程、性方式的描述或者带有性暗示、性挑逗的语言；

4.对性部位描述、暴露，或者只用很小遮盖物的内容；

5.全身或者隐私部位未着衣物，仅用肢体掩盖隐私部位的内容；

6.带有侵犯个人隐私性质的走光、偷拍、漏点等内容：

7.以挑逗性标题吸引点击的；

8.相关部门禁止传播的色情、低俗小说，音视频内容，包括一些电影的删节片断；

9.一夜情、换妻、SM等不正当交友信息；

10.情色动漫，(以露点或者是以漏点用小幅度遮挡为判断)；

11.宣扬血腥暴力、恶意谩骂、侮辱他人等内容；

12.非法性用品广告和性病治疗广告：

13.为经他人允许或利用“人肉搜索”恶意传播他人隐私信息。

三、不得从事下列危害计算机信息网络安全的活动，包括但不限于：

1.未经允许，进入计算机信息网络或者使用计算机信息网络资源的：

2.未经允许，对计算机信息网络功能进行删除、修改或者增加的：

3.末经允许，对计算机信息网络中存储、处理或者传输的数据和应用程序进行删除、修改或者增加的:

4.故意制作、传播计算机病毒等破坏性程序的:

5.其他危害计算机信息网络安全的。

四、承诺在镜像站上播发的信息内容是经当当地宜传管理部门符合/批准的允许内容

五、补充协议

1.反正内容需合法合规

2.不得应用到违规网站，尤其是灰黑产业，不符合工信部或者当地国家规定的项目（

3.项目支持下载，但不能下载违反国家法律法规，你要用就悄咪咪的用，别通过这个链接分享，不该我真的栓Q， 国际站除外

4.未经许可不得再次反向代理该网站 或者反向代理我源站进行二次分发

5.github 项目在不违规的不做任何屏蔽的目的是为了更好的用户体验，麻烦你们不要把我搞得像jsd一样被污染一段时间

6.如果触发防火墙，代表你IP一分钟已经超过2000次，被防火墙的屏蔽被两个三小时之后再试，家庭用户可尝试重启路由器来获取新的IP。或者是保持正常访问。

7.未经允许严禁使用回源其包括但不限于中国香港，新加坡，中国台湾，泰国，孟买，美国，日本，韩国，中国广州，中国成都，等 jsd.cdn.zzko.cn 以及 cdn.jsdelivr.us 还有cdn.jsdelivr.ren 源站集群，

8.您需要理解我们基于合规性每个月不定期都会从cdn平台抽取日志进行抽查，因为大部分流量都不发送请求域名，我们参考加速项目URL地址来

## 平台管理员联系方式与问题反馈 

|QQ|企业微信|github|TG|邮箱|
|-------|---------------|----------|------|------|
|202835956|<img src="https://github.com/54ayao/EdgeJSedSpeed/assets/86733666/aa633562-1b3b-438e-868b-15c0b5a445bd" alt="企业微信">|[点这里](https://github.com/54ayao/EdgeJSedSpeed/issues) |[点这里](https://t.me/boost/jsdmirror)|ayao@cola.email|



首先确认报错
![image](https://github.com/54ayao/EdgeJSedSpeed/assets/86733666/698eecd4-92a7-4fa8-a5e6-04ec72271599)

![image](https://github.com/54ayao/EdgeJSedSpeed/assets/86733666/3806b7e2-a5d9-486b-8311-080db57f3f1b)

以及官方CDN下是否正常使用或者是出现报错 一般情形是我们转发官方头部 如果官方站也是这样需要自行去jsdelivr官方立issues 但是请替换成jsdelivr官方域名反馈 

范文
域名：google.com

节点IP:1.1.1.1

时间:2023年5月4日11:11 

用户省份：中国香港特别行政区

CDN: cloudflare

CDN访问参数（UUID）：abcd1234

是否测试 jsdelivr官方源站：是/jsdelivr官方源站无该报错

使用影响：
无法加载字体 显示cors跨越

