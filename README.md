Removed
V2Ray搭建详细图文教程
233boy edited this page on 2 Jan · 29 revisions
 Pages 5
Find a Page…
Home
V2RayN使用教程
V2Ray一键安装脚本
V2Ray搭建详细图文教程
前言
V2Ray 简介
备注
购买一个VPS
添加到购物车
结算
付款
获取VPS信息
安装 Xshell
登录VPS
安装 V2Ray
V2Ray 安装完成
V2Ray 客户端使用教程
V2Ray 管理面板
TCP 阻断
快速管理 V2Ray
优化 V2Ray
WebSocket + TLS
HTTP/2
mKCP
搬瓦工 VPS 速度慢
Telegram 专用代理
V2Ray 多用户
查看配置 / 修改配置 / 端口 / 传输协议…… ？
哪个传输协议好？
V2Ray 脚本说明
反馈问题
分享
其他
资助 V2Ray
结束
使用Cloudflare中转V2Ray流量
Clone this wiki locally
https://github.com/233boy/v2ray.wiki.git
搭建 V2Ray 看这篇文章就够了！这是完完全全为小白准备的 V2Ray 搭建教程，详细的图文教程确保你可以百分百成功搭建 V2Ray 使用。

前言
此 V2Ray 教程完完全全是为小白准备的，从购买 VPS 到使用 SSH 登录并使用 V2Ray 一键安装脚本配置 V2Ray，详细的图文教程确保你可以百分百成功搭建 V2Ray 使用，哪怕你只是一个小白。
由于 V2Ray 的配置对于小白来说是非常不友好的，所以此 V2Ray 教程的 V2Ray 服务器端配置将会使用我本人撰写的 V2Ray 一键安装脚本，这是一个对小白友好的 V2Ray 一键脚本，简化 V2Ray 安装和部署，并且自动开启 BBR 优化，当然你也可以手动打开 BBR 来优化 V2Ray，也可以选择使用锐速来 优化 V2Ray。

V2Ray 简介
官网：https://www.v2ray.com

V2Ray(Project V) 相对于 Shadowsocks，V2Ray 更像全能选手，拥有更多可选择的协议 / 传输载体 (Socks、HTTP、TLS、TCP、mKCP、WebSocket )，还有强大的路由功能，不仅仅于此，它亦包含 Shadowsocks 组件，你只需要安装 V2Ray，你就可以使用所有的 V2Ray 相关的特性包括使用 Shadowsocks，由于 V2Ray 是使用 GO 语言所撰写的，天生的平台部署优势，下载即可使用，当然啦，由于 V2Ray 的配置相对来说是很繁琐的，毫无夸张的说，但是有了本人所写的 V2Ray 一键安装脚本 加持下，使用 V2Ray 便会显得轻松多了。

备注
总结一下此文章的大致流程，此 V2Ray 教程可百分百帮助你搭建 V2Ray 使用。哪怕你只是一个小白。

购买一个 VPS
想要搭建 V2Ray，就必须要拥有一台 VPS。
获取 VPS 信息
我们必须要知道 VPS IP 地址，root 用户密码，SSH 端口
安装 Xshell
Xshell 是一个 SSH 客户端，要登录 VPS，当然需要 SSH 客户端
登录 VPS
使用 Xshell 配置 VPS SSH 信息，然后登录
安装 V2Ray
安装过程你可以随意选择你喜欢的传输协议或者配置 Shadowsocks
V2Ray 安装完成
此时你可以使用客户端配置 V2Ray 使用了
V2Ray 高级玩法
配置 WebSocket + TLS ， HTTP/2 ， mKCP 等

购买一个VPS
想要搭建 V2Ray， 拥有一个 VPS 是必需的。
我们推荐使用：搬瓦工（Bandwagon Host） VPS 来搭建 V2Ray，搬瓦工是一个对中国用户极度友好的 VPS 商家，有香港，CN2 GIA 等线路，支持支付宝付款，当然也是支持退款的！

备注：按住 Ctrl + 单击， 即可在新窗口打开链接

推荐购买的搬瓦工套餐如下

线路	CPU	内存	硬盘	带宽	流量	价格	链接
香港	2 核	2048 MB	40 GB	1 G	500GB / 月	$89.99 / 月	购买
香港	4 核	4096 MB	80 GB	1 G	1000GB / 月	$155.99 / 月	购买
香港	6 核	8192 MB	160 GB	1 G	2000GB / 月	$299.99 / 月	购买
香港	8 核	16384 MB	320 GB	1 G	4000GB / 月	$589.99 / 月	购买
-	-	-	-	-	-	-	-
CN2 GIA	2 核	1 GB	20 GB	2.5 G	1000GB / 月	$49.99 / 季	购买
CN2 GIA	3 核	2 GB	40 GB	2.5 G	2000GB / 月	$89.99 / 季	购买
CN2 GIA	4 核	4 GB	80 GB	2.5 G	3000GB / 月	$56.99 / 月	购买
CN2 GIA	6 核	8 GB	160 GB	5 G	5000GB / 月	$86.99 / 月	购买
CN2 GIA	8 核	16 GB	320 GB	5 G	8000GB / 月	$159.99 / 月	购买
CN2 GIA	10 核	32 GB	640 GB	10 G	10000GB / 月	$289.99 / 月	购买
CN2 GIA	12 核	64 GB	1280 GB	10 G	12000GB / 月	$549.99 / 月	购买
-	-	-	-	-	-	-	-
日本	2 核	2 GB	40 GB	1.2 G	500GB / 月	$89.99 / 月	购买
日本	4 核	4 GB	80 GB	1.2 G	1000GB / 月	$159.99 / 月	购买
日本	6 核	8 GB	160 GB	1.2G	2000GB / 月	$299.99 / 月	购买
日本	8 核	16 GB	320 GB	1.2 G	4000GB / 月	$589.99 / 月	购买
-	-	-	-	-	-	-	-
CN2	1 核	1024 MB	20 GB	1 G	1000GB / 月	$49.99 / 年	购买
CN2	1 核	2048 MB	40 GB	1 G	2000GB / 月	$52.99 / 半年	购买
CN2	2 核	4096 MB	80 GB	1 G	3000GB / 月	$59.99 / 季	购买
CN2	2 核	8 GB	160 GB	1 G	5000GB / 月	$39.99 / 月	购买
CN2	3 核	16 GB	320 GB	1 G	8000GB / 月	$79.99 / 月	购买
CN2	3 核	16 GB	320 GB	1 G	12000GB / 月	$99.99 / 月	购买
CN2	3 核	16 GB	320 GB	1 G	16000GB / 月	$129.99 / 月	购买
-	-	-	-	-	-	-	-
普通	2 核	1024 MB	20 GB	1 G	1 TB / 月	$49.99 / 年	购买
普通	3 核	2 GB	40 GB	1 G	2 TB / 月	$52.99 / 半年	购买
普通	4 核	4 GB	80 GB	1 G	3 TB / 月	$19.99 / 月	购买
普通	5 核	8 GB	160 GB	1 G	4 TB / 月	$39.99 / 月	购买
普通	6 核	16 GB	320 GB	1 G	5 TB / 月	$79.99 / 月	购买
普通	7 核	24 GB	480 GB	1 G	6 TB / 月	$119.99 / 月	购买
选择哪个套餐？如果你不知道选择哪个套餐
下面这是最常见的购买套餐

线路	CPU	内存	硬盘	带宽	流量	价格	链接
普通	2 核	1024 MB	20 GB	1 G	1 TB / 月	$49.99 / 年	购买
CN2	1 核	1024 MB	20 GB	1 G	1000GB / 月	$49.99 / 年	购买
CN2 GIA	2 核	1 GB	20 GB	2.5 G	1000GB / 月	$49.99 / 季	购买
香港	2 核	2048 MB	40 GB	1 G	500GB / 月	$89.99 / 月	购买
没有找到合适的套餐？你可以前往官网详细查看：https://bwh88.net/cart.php

哪个套餐好？
一般来说，推荐购买 香港线路 或 CN2 GIA 线路，或者哪个便宜选择那个，说着当然如果你使用量比较多或者想要分享给同学和朋友一起用的话，选择合适的套餐即可。又或者你土豪的话，选择最贵的也行。

VPS 速度：香港线路 > 日本线路 > CN2 GIA 线路 > CN2 线路 > 普通线路

香港套餐 VPS 的速度最快。 如果你非常在乎速度的话，建议购买香港线路的 VPS，当然，但价格贵，流量相对其他套餐来说也是比较少的……退一步的选择是 CN2 GIA 线路，这个线路的速度也比较好。

线路是比较重要的，像香港和 CN2 GIA 线路到晚上一般不会怎么炸，例如普通线路到了晚上可能会出现很慢慢的感觉。

我本人比较推荐 CN2 GIA 线路，稳定性，速度与价格适中选择。

当然啦！如果你觉得价格太贵了，推荐你查看一下 Just My Socks ，搬瓦工官方出品的代理服务，优质的 CN2 GIA 线路，每月仅需 $2.88 起！再也不用自己折腾搭建了，最最最最重要的是：被墙自动换 IP，无须担心 IP 被墙！

Just My Socks 购买教程在这里： Just My Socks 购买及使用

毫无疑问！绝对的一分钱一分货。

如果出现 out of stock 这样的提示，那就是这个套餐卖完了，选择其他套餐即可。

添加到购物车
在上面表格中选择想要购买的套餐，然后点击 购买 即可。
将 VPS 添加到购物车

Add to Cart
说明一下，在Billing Cycle选项那里选择：$xxxx USD Annually，按年付的意思

推荐按年付，比按月付最高可省55%的钱

如果你选择购买 CN2 GIA 的线路

在添加到购物车的时候，Location 的选项可以选择 JP - Equinix Osaka Softbank (JPOS_1)

然后点击Add To Cart

结算
推荐使用搬瓦工 6.58% 优惠码：BWH3HYATVBJW

这个优惠码是搬瓦工目前最高优惠的优惠码
输入优惠码之后点击 Validate Code >>

输入优惠码
然后点击 Checkout
如下图所示：已经使用搬瓦工优惠码

Checkout
然后会提示你注册账号 （如果你没账号或者还没登录）
请按照下面图片提示来填写~

Checkout now
要注意的是，Country 选项记得选择 China，Payment Method 选择 Alipay
不要忘了勾上 I have read and agree to the Terms of Service
然后 Complete Order

付款
点击 Pay now
之后便会跳转到支付宝付款界面，完成付款即可

Pay now
获取VPS信息
备注：按住 Ctrl + 单击， 即可在新窗口打开链接

确保你已经成功付款之后
打开：https://bwh8.net/clientarea.php?action=products
选择 KiwiVM Control Panel
如果出现以下界面，稍等一会，等待资源分配即可。

Task in progress
等待两三分钟，刷新一下。
这是已经在运行的界面，请记下 IP address然后点击 stop

停止VPS
当出现：Great Success! Virtual server will stop in a few seconds. 相关提示
证明 VPS 已经停止了，我们需要重装一个系统。点击左边的 Install new OS
之后选择 debian-9-x86_64
再勾上：I agree that all existing data on my VPS will be lost.
然后点击 Reload

Install new OS
当点击 Reload 之后，稍等片刻将会出现下图所示的界面，
请务必记下： You will need a new root password to access your VPS：xxxx
还有：New SSH Port:
一个是root密码，一个是SSH端口

Reload
OK，这时我们已经获取到VPS的信息了。

安装 Xshell
备注：按住 Ctrl + 单击， 即可在新窗口打开链接

Xshell 是一个易用的 SSH 客户端，要登录 VPS，当然需要 SSH 客户端

Xshell 下载链接点我

这是一个绿色版本的 Xshell ，打开链接后，就点击 下载，下载好了之后，就双击打开，然后点击 浏览... 可以选择解压的路径，比如说 D 盘，之后再选择 解压 即可。

解压 Xshell
然后在解压的目录找到 Xshell+Xftp 绿色版本 文件夹，打开它，之后找到 !安装.bat 并且右键选择 以管理员身份运行，安装完成后会有一个提示窗口，关闭即可。这样来就安装好了 Xshell

安装 Xshell
登录VPS
在桌面找到 Xshell ，打开它，新建一个会话。

新建会话
主机写上你的 VPS IP 地址，端口写上 SSH 端口。

new
之后点击 用户身份验证，用户名：root，密码：你的 root 密码。然后点击确定

user-and-passwd
之后选择连接。

连接
然后会提示SSH安全警告，选择，接受并保存。

SSH 安全警告
这是登录成功后的界面

登陆成功
安装 V2Ray
输入下面命令回车，你可以复制过去，然后在 Xshell 界面按 Shift + Insert 即可粘贴，不能按 Ctrl + V 的。。

bash <(curl -s -L https://git.io/v2ray.sh)
如果提示 curl: command not found ，那是因为你的 VPS 没装 Curl
ubuntu/debian 系统安装 Curl 方法: apt-get update -y && apt-get install curl -y
centos 系统安装 Curl 方法: yum update -y && yum install curl -y
安装好 curl 之后就能安装脚本了

然后选择安装，即是输入 1 回车
选择传输协议，如果没有特别的需求，使用默认的 TCP 传输协议即可，直接回车
选择端口，如果没有特别的需求，使用默认的端口即可，直接回车
是否屏蔽广告，除非你真的需要，一般来说，直接回车即可

安装 V2Ray
是否配置 Shadowsocks ，如果不需要就直接回车，否则就输入 Y 回车
Shadowsocks 端口，密码，加密方式这些东西自己看情况配置即可，我个人当然是全部直接回车。。
OK，按回车继续

配置 Shadowsocks
安装信息，如果确保没有什么问题了，按回车继续

安装信息
(备注，安装信息会因你的配置而变化..不用在乎这截图)
(备注，由于我懒…脚本显示的一些信息可能会跟上面的截图有少许不同，但实际上都是很简单明了的)

V2Ray 安装完成
OK，此时 V2Ray 已经安装完成了。

V2Ray 安装完成
如上图所示，V2Ray 配置信息，Shadowsocks 配置信息都有了
如果你使用过 Shadowsocks ，那么现在你可以测试一下 Shadowsocks 配置了，看看是否能正常使用。
如果你使用过 V2Ray 某些客户端，那么现在也可以测试一下配置了。
(备注，可能某些 V2Ray 客户端的选项或描述略有不同，但事实上，上面的 V2Ray 配置信息已经足够详细，由于客户端的不同，请对号入座。)

V2Ray 客户端使用教程
暂停一下，我想，看这篇的孩子多数都是萌新，由于 V2Ray 已经安装完成了，所以此时你应该尝试使用 V2Ray 来连接上真正的互联网了。

Windows
V2RayN使用教程

V2Ray 管理面板
现在可以尝试一下输入 v2ray 回车，即可管理 V2Ray

V2Ray 管理面板
TCP 阻断
如果你觉得你的小鸡出现了这种情况，那么可以尝试使用 UDP 协议相关的 mKCP
当然，用了我的脚本那是很简单的啦，直接输入 v2ray config 然后选择修改 V2Ray 传输协议
之后再选择 mKCP 相关的就行咯
备注：使用 mKCP 或许还可以提高速度，但由于 UDP 的原因也许会被运营商 Qos，这是无解的。

快速管理 V2Ray
v2ray info 查看 V2Ray 配置信息
v2ray config 修改 V2Ray 配置
v2ray link 生成 V2Ray 配置文件链接
v2ray infolink 生成 V2Ray 配置信息链接
v2ray qr 生成 V2Ray 配置二维码链接
v2ray ss 修改 Shadowsocks 配置
v2ray ssinfo 查看 Shadowsocks 配置信息
v2ray ssqr 生成 Shadowsocks 配置二维码链接
v2ray status 查看 V2Ray 运行状态
v2ray start 启动 V2Ray
v2ray stop 停止 V2Ray
v2ray restart 重启 V2Ray
v2ray log 查看 V2Ray 运行日志
v2ray update 更新 V2Ray
v2ray update.sh 更新 V2Ray 管理脚本
v2ray uninstall 卸载 V2Ray

优化 V2Ray
由于本人的脚本在 Debian9 系统会自动开启 BBR 优化加速了，所以不需要再安装 BBR 优化了，
如果你还是觉得网络比较慢的话，你可以尝试使用含有 mKCP 的传输协议，这个 mKCP 的东东，简单一点说就像 Kcptun 一样加速，并且还能进行伪装 (可选)，但是由于 mKCP 是使用 UDP 协议的，也许运营商会限速得更加厉害，网络变得更加慢。但不管怎么样，你都可以随时尝试一下。
服务器输入 v2ray config 回车，然后选择 修改 V2Ray 传输协议，再接着选择 mKCP 相关的传输协议即可
如果你是使用其他商家的 VPS 并且是按照此教程流程来安装 V2Ray 的话，那么你可以输入 v2ray bbr 回车，然后选择安装 BBR 或者 锐速 来优化 V2Ray
只是还想再啰嗦一下，如果你是使用国际大厂的 VPS，并且是按照此教程流程来安装 V2Ray 的话，请自行在安全组 (防火墙) 开放端口和 UDP 协议 (如果你要使用含有 mKCP 的传输协议)

WebSocket + TLS
实现 WebSocket + TLS 超级无敌简单，前提是要拥有一个能正常解析的域名 (并且知道怎么解析域名)
服务器输入 v2ray config 回车，然后选择 修改 V2Ray 传输协议，再选择 WebSocket + TLS，即是输入 4，接着输入你的域名，然后我都懒得说了，脚本都那么简单明了，我还瞎BB干嘛…
哈哈…可能有不少人在折腾 V2Ray 实现 WS + TLS 的时候真的是搞到很蛋痛咯，有些人的教程可能说得不是很清楚，或者是直接忽略小白萌新这些亲爱的用户，嗯，小白们好好加油吧，请尽量多学一些基础知识，别总是做伸手党，对于毫无交集的陌生人，人家并没有任何义务要帮你的啊
偷偷跟你说…使用 WebSocket + TLS 会有断流的问题
多说一句，不要被某些人带节奏，WS + TLS 并不是 V2Ray 的神级配置，该墙还是会墙，墙你不需要理由
备注一下啦，这里我没写怎么教你注册域名啦，怎么解析域名啦，如果你真的想要使用 WebSocket + TLS，那就 自己谷歌摸索一下，其实好简单的啦！
我本人并没有在使用 WS + TLS (WebSocket + TLS)，我用 TCP，就是用一键脚本全程回车的那种懒人

HTTP/2
实现 HTTP/2 (h2) 也超级无敌简单，和 WebSocket + TLS 一样，也就是只要一个域名就够
服务器输入 v2ray config 回车，然后选择 修改 V2Ray 传输协议，再选择 HTTP/2，即是输入 16，然后………看上面的 WebSocket + TLS 的相关。
备注一下，HTTP/2 相比 WS + TLS (WebSocket + TLS) ，在浏览网页时有一些优势。速度是差不多的啦

mKCP
mKCP 这个东东其实就是 KCP 协议，反正你知道是能提速的就行，但是不保证都能提速，还能避免 TCP 阻断，但是也可以会被运营商 Qos.
使用方法：服务器输入 v2ray config 回车，然后选择 修改 V2Ray 传输协议，之后再选择 mKCP 相关的就行

搬瓦工 VPS 速度慢
由于本教程使用了 搬瓦工 VPS 做为教程的一部分，那么相信有些新接触 VPS 的同学可能会是按照教程使用了 搬瓦工 VPS 翻墙。
如果你觉得搬瓦工 VPS 速度慢，你可以尝试修改一下端口，服务器输入 v2ray config ，，然后选择 修改 V2Ray 端口 即可，建议使用常见的端口，比如说 443，当然，为了更加安全隐蔽，你可以直接尝试使用 WebSocket + TLS 或者 HTTP/2 协议，但是使用这两个协议对于没有接触过 域名 的同学相对来说会是比较困难的。
搬瓦工 VPS 速度慢的一个主要原因可能会是因为端口限速，如果你已经修改端口为 443，速度还是慢的话，我建议你尝试使用 mKCP 协议。

Telegram 专用代理
重要提醒：不建议使用 V2Ray 的 MTProto 代理！
推荐使用： https://github.com/cutelua/mtg-dist

如果你在使用 Telegram 的话，你可以配置一个 Telegram 的专用代理，这样来，在某些情况下你就不需要再开一个代理软件了。
输入 v2ray tg 即可配置 TG 专用代理
配置 Telegram MTProto

配置Telegram MTProto
Telegram MTProto 配置信息

Telegram MTProto 配置信息
V2Ray 多用户
目前此 V2Ray 一键脚本只支持配置一个 V2Ray 账号…一个 Shadowsocks 账号
说着当然，如果你是大佬，配置 多用户 这种事，不是分分钟的事么？

查看配置 / 修改配置 / 端口 / 传输协议…… ？
请看上面的快速管理。。。或者直接输入 v2ray 回车，找到你想要执行的功能。

哪个传输协议好？
心中无杂念，用 TCP
ISP 常作怪，用 动态端口
小鸡速度不好，用 mKCP
处子之身，用 WS + TLS

V2Ray 脚本说明
V2Ray 一键安装脚本

反馈问题
请先查阅：V2Ray 一键安装脚本疑问集合
Telegram 群组： https://t.me/blog233
Github 反馈： https://github.com/233boy/v2ray/issues
任何有关于 V2Ray 的问题，请自行到 V2Ray 官方反馈。
目前只支持配置一个 V2Ray 账号…一个 Shadowsocks 账号。。不支持 SSR。。

分享
如果这篇文章对你帮助的话，记得分享给你的小伙伴们。

其他
请勿违反国家法律法规，否则后果自负！
低调低调低调。

资助 V2Ray
如果你觉得 V2Ray 很好用，能解决你的某些问题，请考虑 资助 V2Ray 发展 。

结束
我有写少了什么吗？我这种小小白萌新看了这教程都觉得很明白了啊。
一次不会，那么就两次，还是不会，那就再来一次。可还是不会啊？大佬请收下我的膝盖。

担心 IP 被墙？或者不想 IP 被墙？是的！使用 Cloudflare 来中转 V2Ray 的 WebSocket 流量就行！由于使用了 Cloudflare 中转，所以墙根本不知道背后的 IP 是多少，你可以愉快的玩耍了~

提醒
如果你不是使用 移动宽带 的用户，那么使用 Cloudflare 中转的速度相对来说是比较慢的，这个是因为线路的问题，无解。
警告警告警告
该教程目前写得比较简陋，以后应该会增加详细图文教程
V2Ray 的 WS + TLS 不是神话，如果你没学会走路就不要急着跑
大佬。。。你如果是从来没接触过 V2Ray 的人一上来就开玩 WS + TLS
你真的不怕摔跤吗
你有解析过域名吗，知道什么是 A 记录吗，会修改 NS 吗。。
如果不懂，那就先补上这些知识再往下看
如果实在想玩 WS + TLS，请认认真真看教程
教程真的写得比较简陋，如果实在折腾不成功，那也很正常的，改天再来
或者直接放弃

这是一个提示
真是无聊，折腾啥啊。买个搬瓦工 Just My Socks 先凑合用着就可以了，被墙自动换 IP，无须担心 IP 被墙！Just My Socks 是搬瓦工出品的代理服务，质量可靠，优质 CN2 GIA 线路，并且支持退款，放心无忧。
套什么 CF，速度慢到怀疑人生。

准备
一个域名，建议使用免费域名
确保域名已经可以在 Cloudflare 正常使用。
在 Cloudflare 的 Overview 选项卡可以查看域名状态，请确保为激活状态，即是： Status: Active
怎么 SSH 连接上被墙的 IP ? Xshell 在属性那里可以设置代理，或者你可以在一台没有被墙的境外 VPS 使用 iptables 转发数据到被墙的机器上，此处不细说了。

添加域名解析
在 DNS 选项卡那边添加一个 A 记录的域名解析，假设你的域名是 233blog.com，并且想要使用 www.233blog.com 作为翻墙的域名
那么在 DNS 那里配置，Name 写 www，IPv4 address 写你的 VPS IP，务必把云朵点灰，然后选择 Add Record 来添加解析记录即可
(如果你已经添加域名解析，请务必把云朵点灰，即是 DNS only)

OK，确保操作没有问题的话，继续

安装 V2Ray
如果你已经使用本人提供的 V2Ray 一键安装脚本并安装了 V2Ray，那就直接输入 v2ray config 修改传输协议为 WebSocket + TLS

如果你并没有使用本站提供的 V2Ray 一键安装脚本来安装 V2Ray
那么现在开始使用吧，最好用的 V2Ray 安装脚本，保证你满意
使用 root 用户输入下面命令安装或卸载

bash <(curl -s -L https://git.io/v2ray.sh)
如果提示 curl: command not found ，那是因为你的小鸡没装 Curl
ubuntu/debian 系统安装 Curl 方法: apt-get update -y && apt-get install curl -y
centos 系统安装 Curl 方法: yum update -y && yum install curl -y
安装好 curl 之后就能安装脚本了

之后选择安装，传输协议选择 WebSocket + TLS (即是选择 4 )，V2Ray 端口随便，不要是 80 和 443 即可，然后输入你的域名，域名解析 Y ，自动配置 TLS 也是 Y ，其他就默认吧，一路回车。等待安装完成
如果你的域名没有正确解析，安装会失败，解析相关看上面的 添加域名解析

安装完成后会展示 V2Ray 的配置信息，并且会询问是否生成二维码等，不用管它，直接回车

然后输入 v2ray status 查看一下运行状态，请确保 V2Ray 和 Caddy 都在运行

如果没有问题的话，继续

设置 Crypto 和 开启中转
确保 Cloudflare 的 Crypto 选项卡的 SSL 为 Full
并且请确保 SSL 选项卡有显示 Universal SSL Status Active Certificate 这样的字眼，如果你的 SSL 选项卡没有显示这个，不要急，只是在申请证书，24 小时内可以搞定。

然后在 DNS 选项卡那里，把刚才点灰的那个云朵图标，点亮它，一定要点亮一定要点亮一定要点亮

云朵图标务必为橙色状态，即是 DNS and HTTP proxy(CDN)

V2Ray 配置信息
很好，现在接下来配置客户端使用
输入 v2ray info 即可查看 V2Ray 的配置，如果你有使用某些 V2Ray 客户端，可以根据给出的配置的信息来配置使用了。赶紧测试吧

V2Ray 客户端使用教程：
Windows
V2RayN使用教程

什么鬼？对啊，就是如此简单啊，要不然你以为啊。

备注
如果你的 VPS 位置是在美国西海岸的话，速度应该还算可以吧，如果不是在美国西海岸，那么也许速度会很慢，不过好在不用担心 IP 被墙或者能让被墙的 IP 重生也挺好的。难道不是么？
如果你使用移动网络的话，那么 Cloudflare 的中转节点可能会在香港，速度也许会不错 (不完全保证)。

无限域名备用
懒得写了，自己悟吧…
反正绝大多数人只要知道怎么把墙的 IP 救活就行…
算啦，我还是提示一下吧，WebSocket 协议，80 端口，Cloudflare 的 Crypto 选项卡 SSL 为 Flexible
如果没有太多必要，不需要折腾这

结束
哇，没有图文教程你就看不懂的话，我能怎么办，我也很绝望，我更加迷茫


