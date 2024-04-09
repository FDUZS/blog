---
title: "越过长城，走向世界"
date: 2024-03-20T14:34:55+08:00
summary: Across the Great Wall, we can reach every corner in the world.
draft: false
tags: ["Internet"]
cover:
    image: "<image path/url>"
    alt: "<alt text>"
    caption: "<text>"
    relative: false
    hidden: true
---

*Across the Great Wall, we can reach every corner in the world.* 这句话为上世纪八十年代中国与国际计算机网络连接时发出的第一封电子邮件，而今看起来不无讽刺意味。

### 起

不太记得是什么时候、因为什么开始寻找“翻墙”工具的，但我觉得这跟饿了要吃饭、渴了要喝水一样正常。墙就在那里，你要找的东西就在墙外，怎么办？

一开始根本分不清什么是代理、什么是 VPN，只记得从计算机学院学长那儿拿了个叫“赛风”还是“蓝灯”的软件，一运行就能让我访问那些在大陆互联网上“不存在”的网站。

在这之后很长一段时间，我用的都是这两个免费软件，手机上也不例外。当然，手机上的选择可能多点，毕竟谷歌应用商店类似免费 App 不少。期间想过购买一些专业 VPN 服务，但因为支付工具和价格的原因作罢。但也因此，我的 PayPal 账号算是注册得比较早的。

这一阶段的需求总体来说比较简单，只要能连上、能打开就行，不在乎什么速度。

### 承

时间大致来到了 2016 年暑假，买了台[搬瓦工][BandwagonHost] VPS 并参照教程成功搭建了第一个代理。之后断断续续大概用了三年搬瓦工，眼看着他一步步涨价直到失去性价比。大概 17 年同时使用 DGCHost，跑路之后用了一年的 [GGC][GigsGigsCloud]，直到 2019 年三十周年时代理服务器 IP 第一次“被墙”，中间还经历了 GreenVPN 停止服务。在这之后，基本没有再把自建代理当成主力使用。

其他用过的大大小小的 VPS 服务商包括 [Vultr]、[DigitalOcean]、[RamNode] 等。这一阶段的主要需求是网页浏览和 YouTube 等平台，Netflix 等流媒体平台用得不多。主要特征是一键脚本安装，单节点和 IP 直连。

### 转

2019 年的夏天，开始转向使用“机场”，桌面软件也从之前的 shadowsocks 换成了带订阅功能的 shadowsocksr-csharp 以及正在用的以分流著称的 Clash 系列。相比之下，v2ray 系列客户端用得很少。

一开始用的是 [IPLC.VIP] 这家，使用体验我觉得很好，无论是节点质量还是客服响应速度。此后，和朋友合租过 N3RO 和 PieCloud 这两家机场，使用体验稀烂。尤其是后者，本身节点就不多，还经常有半数掉线。目前，合租的机场是 [WestData]，绝对是便宜大碗的代名词。我个人在用的机场有很多，包括 [FlowerCloud]、[MESL] 和 [Just My Socks]。

除此之外，自建节点并套用 CDN 在当下也是常规操作。这一阶段需求很复杂，对不同类型流量进行分流，Clash for Windows 的 TUN 模式接管那些不遵循系统代理的软件流量以避免手动设置各种代理和更换镜像源等。

### 合

Fuck GFW!

[BandwagonHost]: https://yourl.ink/bwg
[GigsGigsCloud]: https://yourl.ink/ggc
[Vultr]: https://yourl.ink/vultr
[DigitalOcean]: https://yourl.ink/do
[RamNode]: https://yourl.ink/ramnode
[IPLC.VIP]: https://yourl.ink/iplc
[WestData]: https://yourl.ink/westdata
[FlowerCloud]: https://yourl.ink/flowercloud
[MESL]: https://yourl.ink/mesl
[Just My Socks]: https://yourl.ink/jms
