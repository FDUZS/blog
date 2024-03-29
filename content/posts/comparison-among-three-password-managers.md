---
title: "1Password、Enpass、Bitwarden 使用体验之比较"
date: 2019-12-30T23:37:10+08:00
summary: 一篇关于三款密码管理工具主观不全面，偏体验和细节的比较评测，主要从价格、同步情况、密码填充和界面等方面展开。
draft: false
tags: ["Password Manager"]
---

半年多前，一次偶然机会得知 1Password（下称 1P）提供一年的家庭版试用机会，到期后付费也就不到 60 美元 / 年（个人版不到 36 美元），并不算贵，于是便注册了个账号开始尝试使用密码管理软件。我算是比较谨慎的人，自从接触网络以来没有使用过弱密码，最开始使用的也含有十位以上的数字字母，后来加入了特殊字符以及逐渐演化出的一套自定义密码规则和根据账号重要程度的三级密码分级制度。这算是在使用 1P 前我自认为比较完善的密码管理方法，兼顾了密码记忆难度和安全性。但是，有时候账号的重要程度是无法严格区分的那么后期记忆的时候就有可能用错不同等级的密码，此外不同应用（网站）对密码的要求不一样（有不少不支持密码中含有特殊字符的，又或者我自定义的密码规则超出了最大长度只能删减或者降低密码等级缩短长度），还有就是如果开启 TOTP 验证必须安装诸如 Google Authenticator 的应用非常麻烦（麻烦之处有二：一为填写验证码时必须拿出手机而无法直接在桌面电脑上完成，二则是考虑到同步及意外情况需换用支持 TOTP 验证同步的应用。虽然与「不将鸡蛋放在一个篮子里」相悖，但我曾遇到过这类意外和通过申诉、人工服务等找回密码的窘境，所以同步功能自然在我考虑范围之内）。

说回到密码管理软件，1P 确实改变了我的密码管理习惯并且极大地提高了生活幸福感。比如，新注册的账号我都直接用 Password Generator 生成 24 位（如果支持的话，否则减少长度）含大小写字母、数字、特殊字符的随机密码，我可以毫无顾忌地开启 TOTP 验证，发现哪些密码是多个账号共用的，通过浏览器插件一键填充，支持通过 Windows Hello、Face ID 解锁等。但是，就 1P 而言，它并不完美。首先，同步速度真的是不敢恭维，有时必须得退出应用后重新启动它似乎才会反应过来；然后是保存的 Item 中有些网站应用的图标无法成功抓取只留一个「小锁」，这对于强迫症患者来说是非常抓狂的；再有就是关于密码分享的，比如我将我 Private Vault 中的某个账号密码分享给家人后在 All Vaults 中会显示两个（一个在 Private，一个在 Shared），这是正常的。但是，当我修改 Private Vault 中这个账号某些信息后，我所期望的是 Shared Vault 中该账号信息也随之变化，但事实并非如此。我得先将原来共享的删除后，再重复一次共享操作。这有点像「浅拷贝」和「深拷贝」的区别，不知能否明白我的意思。

![1Password-Generator](https://img.shuaizheng.org/2307/1Password-Generator.png)

除了上面提到的三个痛点，1P 确实是我今年尝试过的最爽的应用之一。但人嘛，总想追求最好的，即使可能并不存在或者这已经是最好的。于是，在一众密码管理软件中，我努力寻找属于我的那一个。我首先剔除了 LastPass（出过安全事故）和 KeePass（首先自然是 Windows 下的 UI 不讨喜，其次是以插件的形式添加功能需投入很多时间打磨，以及各个平台客户端的设计风格不统一），SafeInCloud、Dashlane 等之前听得比较少，最后考虑到时间成本等因素只挑选了 Enpass 和 Bitwarden 加入比较。同时，由于手上只有 Windows 笔记本和 iPhone，故无法对 macOS、Linux 和 Android 下的使用表现进行评价。所以，这是一篇主观不全面，偏体验和细节的比较评测。

### 收费模式

- **受限的免费版**：在提供免费版本上，各家也有不同的思路。比如，1Password 只提供 30 天试用而没有可供免费使用的「阉割版」。Enpass 则是桌面端、移动端都提供全功能的免费版本，但是移动端免费版本能保存的密码条数最多只有 25 条且只有一个 Vault。Bitwarden 的思路又不同，它提供免费版本且对密码条数没有限制，但是某些功能只有高级账户才能使用，其中就包括对我来说非常关键的 TOTP 认证。此外，像密码泄露检查、弱密码和多账号共用密码检查等也需要高级账户才能解锁。

- **订阅制**：1Password 是这三者中最贵的，个人版年付 2.99 美元 / 月，家庭版年付 4.99 美元 / 月。Enpass 年付 0.99 美元 / 月，现在还有圣诞节半价优惠。Bitwarden 则是个人版 10 美元 / 年，家庭版 1 美元 / 月。

- **一次性买断**：Enpass 是三者中唯一仍旧提供买断制的，平常价格为 49.99 美元，同样现在半价优惠为 24.99 美元。

### 数据存储和同步方式

- **本地存储 + WebDAV/Dropbox**：同样，这三者中 Enpass 又是比较特别的一个，它的密码可以完全只存放在本地，也可以借助 iCloud、Dropbox 等云存储同步，还支持 WebDAV。那么，借助 WebDAV 可以将密码通过坚果云来同步，极大加快了同步速度，解决了上面提到的使用 1P 时同步慢的问题。

- **官方服务器**：默认情况下，1P 和 Bitwarden 都是通过官方服务器来同步密码的，我感觉这俩的速度都差不多，可能后者要快那么一点。当然，有此感觉也可能是对 1P 的龟速怨念所致。

- **自建服务器**：Bitwarden 的服务端、桌面端、移动端等都是开源的，它也非常慷慨大方地提供了通过 Docker 来自行部署的[方法](https://help.bitwarden.com/article/install-on-premise/)，并且全过程非常地简单。唯一的一点就是，要求服务器的内存至少 2GB。但是，有个兄弟用 Rust 实现了这一功能，并将[源码](https://github.com/dani-garcia/bitwarden_rs)公布在 GitHub 上，对服务器的要求大大降低。我在按照官方教程[部署](https://bitwarden.iamzs.ga/)（**开放至 2020/01/03 24:00:00**）完之后，与 [bitwarden_rs 版](https://pwd.iamzs.ga/)（**开放至 2020/01/03 24:00:00**）比较发现，在前者中那些高级账户的 features 仍然没有解锁或者说是根据你注册时使用的邮箱来决定是否解锁（邮箱账号是否已经是 Premium），而在 Rust 版中所有的功能都是可以直接用的。此外，在搭建过程中还是遇到不少坑的，比如通过官方的 Docker 安装后一直无法收到 Verification Email，后百般尝试才解决。搭建过程和踩的坑可能会另写一篇文章。

更新：在删除测试用的密码时，我发现似乎官方版 Docker 搭建的同步和响应速度要快些，不知是不是心理作用。

更新：不得不说，官方版吃内存真是猛啊……

![GCP](https://img.shuaizheng.org/2307/GCP.png)

### 密码填充

作为密码管理软件的核心功能，我反而觉得没有什么可说的。如果连密码填充都做不好的话，还有什么必要选它呢。这三者的密码填充方式也不太相同，Bitwarden 属于一次点击自动填充，Enpass 默认设置是双击自动填充并提交。1P 可能是因为我最先使用且已经全面接管了谷歌浏览器的「自动填充」，在网页表单右侧会驻留一个「小锁」并显示填充浮窗，单击即可完成填充，如果开启了 TOTP 会连 one-time password 也一并复制供后续填充。

![1Password-Chrome](https://img.shuaizheng.org/2307/1Password-Chrome.png)

![1Password-Web-Form](https://img.shuaizheng.org/2307/1Password-Web-Form.png)

但，以上所述功能在这三款软件使用期间均遇到抽风的情况。

### 用户界面

就 Windows 下来说，我觉得 1P 和 Bitwarden 的界面都还可以，但是不太喜欢 Enpass，它的设计风格 Windows 气息太浓了，没阴影、没圆角、没渐变，丑拒。

![1Password-PC](https://img.shuaizheng.org/2307/1Password-PC.png)

![Bitwarden-PC](https://img.shuaizheng.org/2307/Bitwarden-PC.png)

![Enpass-PC](https://img.shuaizheng.org/2307/Enpass-PC.png)

iOS 下其实也和 PC 下差不多，Enpass 我感觉依旧最丑，虽然比 Windows 版好看了一点。不过，下图一最左侧 Face ID 解锁 Enpass 时下面的一大块黑真的是辣眼睛。

![Enpass-iOS](https://img.shuaizheng.org/2307/Enpass-iOS.JPG)

![1Password-iOS](https://img.shuaizheng.org/2307/1Password-iOS.JPG)

![Bitwarden-iOS](https://img.shuaizheng.org/2307/Bitwarden-iOS.JPG)

在功能布局上，三者的侧重点也不一样。Enpass 的底栏分别是所有密码条目按字母升序（左上角同步，右上角可以新添密码）、分类标签页和 TOTP 及附件查看（乱七八糟）、密码检测和生成页、设置页，给我的感觉就是页面功能分类不清和重复多余。比如说，我觉得 All Items 页和 Groups 可以合并在一起，将搜索框、同步按钮及新增按钮挪到 Groups 中去。相比之下，我觉得 1P 的思路可能更好一下，虽然它也有四栏，但却不会给我凌乱的感觉。第一栏中显示的是加星的那些密码项和最近使用过的，同时还提供了搜索框。第二栏是分类页，右上角可以新增条目且同样可以检索密码项。第三栏就比较特别和有意思，它是一个标签页，虽然我这里目前是空的，但可以想见即使以后添加了各种标签大概率一页也足够全部显示，不会显得繁杂。但是，前面的「分类」和这里的「标签」是否也存在重复呢，仔细观察的话会发现很多软件中都有这二者共存的现象，找机会我得好好研究一下。第四栏设置页就不多说了。Bitwarden 是这三者中界面最简洁的，第一栏将分类和具体密码项放在一起，顶部是搜索和新增按钮，第二栏就完全只是一个密码生成器，最后一栏同样是设置页。我不是很认同其第二栏的做法，就我来说移动端功能基本就是填充密码，像注册账号生成密码之类的工作都会在桌面上完成，所以对我来说将这一功能单独放在一栏完全没必要。

### 一些重要的细节

- **Website Icon 的获取逻辑**：1P 在这方面的表现应该是最差的，一开始在「三个痛点」中就有提到，另外两款软件都能获取到偏偏它不行。Enpass 和 Bitwarden 在抓取逻辑上也存在不同。就我不严谨观察发现，在 [https://mail.zju.edu.cn](https://mail.zju.edu.cn) 的抓取上两者表现不一样，Enpass 抓取的图标居然是浙大的校徽「求是鹰」，而这是 [https://www.zju.edu.cn](https://www.zju.edu.cn)的 icon，与之相对 Bitwarden 则正确抓取了「邮件」icon。但是，这俩货在别的网站上抓取的好像又是一样的，不知为何。

- **「复制」操作后的反馈**：Bitwarden 的反馈是最好的，你分别复制 Username、Password、Website 项，得到的反馈也一一对应：Username copied、Password copied、Website copied。其次是 Enpass，它虽然有明显的反馈但是你无论是复制什么，它只会告诉你 Copied to Clipboard。相比之下，1P 的反馈就没有那么明显，只是表单字段底色变成深色。

- **表单字段抓取**：我觉得 Enpass 在这方面的表现是最差的。下图是我完全使用 Enpass 注册的一个账号（密码生成 + 表单抓取保存），当你点开「Show Webform」时会发现它抓取了很多不必要的信息并且需要经常到「FORM MAPPING」中进行调整（因为有些网站注册时需要填用户名、邮箱、密码等信息，但是登录时「用户名」只能是邮箱而不是前述用户名，但 Enpass 填充时会将用户名填入表单）。

![Enpass-Webform](https://img.shuaizheng.org/2307/Enpass-Webform.png)

并且，在应对像 Box 这类[登录页面](https://account.box.com/login)时，Enpass 显得更加力不从心。这类登录页面有这样一个特点，你需要先填写用户名（Username/Email），点击下一步后才会出现密码框和登录按钮。起先我以为这样设计，Box 会先对输入的用户名进行核验，后来发现其实不会，那我就不是很明白这样操作的意义了。

![Box-login](https://img.shuaizheng.org/2307/Box-login.png)

那么，Enpass 会抓取些什么呢？下面是谷歌浏览器 Enpass 插件提示我保存的 Item，发现漏掉了用户名（此处为 Email），我觉得是不堪使用的。

![Enpass-Add-Item](https://img.shuaizheng.org/2307/Enpass-Add-Item.png)

- **Item 自动命名**：在这一项中，我最喜欢 Bitwarden 的处理方式，它的 Item Name 使用的都是登录网站的域名，比如登录的 Website 为 `mail.zju.edu.cn`，那么其 Item Name 就同样是 `mail.zju.edu.cn`。这对于一个强迫症患者来说真的是无比舒适。1P 默认抓取的应该是 `head` 标签下 `title` 标签的值，中规中矩。我最不喜欢的是 Enpass 的处理方式，它同样是根据登录网站的域名来确定 Item Name 的。只不过，我认为它的做法有点简单粗暴甚至自以为是，直接截取域名的二级域，然后首字母大写其余一律小写。仍旧以 `mail.zju.edu.cn` 为例，那么它默认保存的 Item Name 为 `Zju`，对这种做法我只能呵呵。

![Bitwarden-Items](https://img.shuaizheng.org/2307/Bitwarden-Items.png)

![Enpass-Items](https://img.shuaizheng.org/2307/Enpass-Items.png)

- **TOTP 添加方式**：Windows 下除 1P 可以扫描二维码外，其余两个都必须手动输入 code 或者掏出手机来扫码。虽然 1P 有些二维码也不能直接识别必须借助手机，但是有总比没有好，还是必须给好评的。

- **单击 Tray Icon 后的表现**：Enpass 又是个奇葩，你无论是左键单击还是右键单击任务栏的图标，它的表现都是一样的：打开它的 mini 界面，类似于 1P 中的「1Password mini」。我们平常所养成的习惯或者遵循的惯例是，`右键单击任务栏图标退出软件`，但我们若想退出 Enpass 还得再多一步操作，加上不区分左右键单击功能，我认为不太合理。另外两个就很好。

### 我的选择

首先自然不会选 Enpass，除了支持 WebDAV 和一众网盘同步，提供一次性买断外，好像找不出什么优点甚至全是缺点了。我纠结的其实是 1P 和 Bitwarden，前者的诸如弱密码、共用密码检测可以直接在桌面端查看，但这些属于 Bitwarden Premium 才能解锁的 feature 且只能在 Web 端查看。通过 Bitwarden 官方 Docker 镜像自建同样需要升级到 Premium，Rust 版其实又不太放心（后期官方调整更改 API），还需支付服务器的费用，虽然不是什么事。价格的话，其实一年 10 刀跟一年 36 刀我觉得没有什么差别，这样想来，我为何觉得手上的 1P 更香了，只不过还是得忍受它的几个缺点。至于 Bitwarden，真的没什么缺点（虽然同步速度也不太行），可玩性又很大，比如在搭建过程中温习了 Docker 相关知识，应当持续关注。
<!-- 
### 致谢

- 感谢 Enpass、Bitwarden、1Password 开发者开发出这么好用的工具，虽然我注定和你们其中二者分手，但你们依然是好人

- 感谢 Google Cloud Platform 慷慨提供的 300 美元赠金，测试所用的 4C4G 和 1C4G 虚拟服务器来自于此

- 感谢坚果云对 WebDAV 的支持

- 感谢阿里云免费使用的邮件推送服务

- 感谢 Freenom 提供的免费域名

- 感谢 Cloudflare 提供的免费域名解析

- 感谢 Docker 及 bitwarden_rs 开发者 -->
