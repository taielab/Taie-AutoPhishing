## 前言

针对企业的网络钓鱼攻击都在发生。有些钓鱼涉及电子邮件和网站，有些通过移动APP或社交媒体平台，还有些可能会使用短信甚至是电话。使用方式不一，本文此次主要是探讨钓鱼攻击多点的基础设施快速建设，这个点的需求对于日常红蓝对抗中，基建起的比别人快那么你们的机会也会得到的比别人更快和更多。临时去部署基础设施可能还会遇到各种各样的问题不一定能去都解决掉，所以引出本文的出现。关于钓鱼的基础概念和常见的攻击手段不在本文中重复叙述。只要给各位开拓一下思路，可能是有的点是各位没有去接触过利用过的效率点

## 常规钓鱼思路

### VPS基建部署

可以选择一键lnmp脚本，切记！ 切记！ 切记！做好高强度加固防止被反打！

### 钓鱼文档制作

可以根据蓝方政企的历史泄露比如百度云上的泄露的一些文档或者官网上的一些文档从中提炼出符合对方政企的文档格式要求。或根据对公司的企查查上的一些负面消息去做一些文章。方法不一看各位经验。

附上一个常见参考的政企公文文档网址方便精准提取信息

地址：http://gongwenguan.com

### ditto

Ditto是一个小型工具，它接受域名作为输入，并为[同形异义词攻击](https://en.wikipedia.org/wiki/IDN_homograph_attack)生成其所有结果作为输出，并检查哪些可用和哪些已经注册。

简单来说就是你拿到你想钓鱼的蓝方的域名去利用他快速生成高相似度的钓鱼域名去注册可用的来伪装去骗其蓝方公司安全意识不强的员工来达到你的钓鱼目的。

地址：https://github.com/evilsocket/ditto

### SiteCopy

网站复制，也可称为网站备份。是通过工具将网页上的内容全部保存下来。当然不仅仅只是保存了一个html页面，而是将网页源码内所包含的css、js和静态文件等全部保存，以在本地也可以完整的浏览整个网站。

通过它快速拿到钓鱼点的前端源码对其进行修改转换PHP或者JAVA修改前端的请求参数和method入口到后端写个api接口接收前端的传参，还可以额外加上获取请求者的IP和UA方便进一步利用。常用的钓鱼点比如OA，邮服，管理平台等等，可以提前准备市面上常见的OA，邮服，管理平台之类的钓鱼点改造的储备。

还有其他同样优秀的仿站小工具比如：https://smalltool.github.io/也是一款不错的快速拉钓鱼点源码的效率工具，或者通过Linux下的wget扒站也是一个不错的方式。

 地址：https://github.com/Threezh1/SiteCopy.git

### PhishingLogin

脚本作用主要用来接收钓鱼页表单里输入的账号密码,要接收的参数均可根据自己的是需求进行添加,脚本写的粗糙,请弟兄们自行改进
另外,也可把自己的JS探针直接查到钓鱼页里,顺手搜集目标机器信息,实际中尽量用最少的操作去搜集尽可能多的信息

地址：https://github.com/fuzz-security/PhishingLogin.git

### formphish

基于网络钓鱼表单的自动网站。该工具可以自动检测基于html表单的网站上的输入，以创建网络钓鱼页面。

地址：https://github.com/t3rm1naLdr01d/formphish

### 邮服发信平台

一键大家邮服可用发送钓鱼邮件

地址：https://github.com/sumerzhang/PhishingInstall.git

### 邮服探针

邮箱探针后台管理系统，此探针可以判断目标是否点击了邮件。

地址：https://github.com/r00tSe7en/Mail-Probe.git

### espoofer

*espoofer*是一个开源测试工具，可以绕过电子邮件系统中的SPF，DKIM和DMARC身份验证。它可以帮助邮件服务器管理员和渗透测试人员检查目标电子邮件服务器和客户端是否容易受到电子邮件欺骗攻击或是否可以被滥用来发送欺骗电子邮件。

地址：https://github.com/chenjj/espoofer.git

### PhishAPI

全面的基于网络的网络钓鱼套件，可快速部署和实时警报！该API具有三个主要功能。一种允许您轻松地部署克隆的登录页面以进行凭据窃取，另一种是武器化的Word文档创建，第三种是保存的电子邮件活动模板。两种攻击方法都集成到Slack中以进行实时警报

地址：https://github.com/curtbraz/PhishAPI.git

## 非常规钓鱼思路

### QRLJacking

QR二维码钓鱼

https://github.com/OWASP/QRLJacking.git

### lockphish

在锁定屏幕上进行网络钓鱼攻击的工具，旨在使用https链接获取Windows凭据，Android PIN和iPhone Passcode。这个点可能还需要很多时间去打磨直接丢过去可能对方不会看。

地址：https://github.com/JasonJerry/lockphish.git

### hmmcookies

使用快捷方式文件（绕过UAC）从Firefox，Chrome，Opera抓取Cookie

地址：作者已删库源码本地我存了一份，这个钓鱼点我暂时还没想清楚具体实施的有效性是多少

### asnphishing

具有otp绕过功能的高级网络钓鱼工具，当蓝方人员输入其凭据时，您需要转到原始网站并使用这些凭据将真实的OTP发送给受害者。一旦他输入该OTP，该OTP也将与您同在，您将被允许在他之前登录该帐户。

地址：https://github.com/asnzodiac/asnphishing.git

## 更多内容关注官方公众号：

![](weixin2.png)