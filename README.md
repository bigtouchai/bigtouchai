自建Vless WS TLS节点，并开启CDN提升节点防护，完整教程！
xiaochaib edited this page on Sep 11, 2023 · 12 revisions
请配合视频教程食用：https://youtu.be/eqYL6P6T9sU

VPS服务器购买
自建节点需要有一台VPS服务器，如想月付，可使用Vultr家的VPS服务器，Vultr官网，2014年成立，性价比高，目前月付3.5刀/月，可随时免费更换IP、不用担心IP不够用，机器、网络运行稳定性佳，并且提供超过32个机房可选，支持支付宝。

如果追求极致速度，也可考虑使用搬瓦工VPS。搬瓦工VPS官网，以下是推荐用来自建节点的机房，可点链接直达。
搬瓦工VPS订购、部署机器、服务器登录信息获取指引！

线路名称	处理器	内存大小	硬盘容量	带宽	流量	价格	链接
CN2	1 核	1024 MB	20 GB	1 G	1000GB / 月	$49.99 / 年	购买
CN2 GIA	2 核	1 GB	20 GB	2.5 G	1000GB / 月	$49.99 / 季	购买
香港	2 核	2048 MB	40 GB	1 G	500GB / 月	$89.99 / 月	购买对于绝大多数用户来说，CN2线路已经满足；非常追求超极致速度、钱包厚的朋友可以选择CN2 GIA或香港线路
如果跳转到购买链接提示：Out of Stock说明没库存了，香港机一般很紧俏
搬瓦工优惠码：**BWHNCXNVXV**
如果真的不想自建，想用机场，那么我推荐你使用搬瓦工官方JMS机场，非常稳定、不跑路！
搬瓦工JMS机场使用图文指引！点我~

域名购买、托管到CloudFlare
域名注册、购买，推荐使用namesilo，免费的whois隐私保护！
NameSilo官网（域名）：namesilo官网
PING工具：ping工具（检测解析域名是否生效）
CloudFlare(套CDN)：CF官网）

# SSH连接工具
任选其中一个即可
FinalShell(推荐、全平台):FinalShell下载
MobaXterm:MobaXterm官网

安装V2Ray
1、必要更新操作(Debian/Ubuntu)
apt update -y && apt install -y curl socat wget
**注意：**如果是centos系统，则分别运行yum update -y和yum install -y curl socat wget

可选操作：部分VPS服务器需要开放端口（搬瓦工已默认开放所有端口,所以此步不需要）
一些服务器的端口需要手动开放，像Vultr，需要安装防火墙（CentOS运行yum install firewalld安装）
请参考此篇开放端口:VPS开放端口

正式安装V2Ray(使用233Boy大佬的一键脚本)
系统支持：Ubuntu，Debian，CentOS，推荐使用 Ubuntu，谨慎使用 CentOS，脚本可能无法正常运行！
执行如下命令：

bash <(wget -qO- -o- https://git.io/v2ray.sh)
管理面板
安装完成后，输入 v2ray 就能看到管理面板，如下图片所示 image

V2Ray 脚本管理面板 提示，如果你不想执行任何功能，直接按 Enter 回车退出即可。

BBR加速
四合一 BBR Plus / 原版BBR / 魔改BBR一键脚本（Centos 7, Debian 8/9, Ubuntu 16/18 测试通过）

wget -N --no-check-certificate "https://raw.githubusercontent.com/chiakge/Linux-NetSpeed/master/tcp.sh" && chmod +x tcp.sh && ./tcp.sh
客户端下载
V2Ray-windows客户端：v2rayN下载
安卓：V2RayNG
苹果MAC OS：V2RayU下载
IOS：App Store中，登录非国区账号，安装Shadowrocket小火箭（推荐，协议支持全面、便宜）
不管是iPad平板还是iPhone手机，比较推荐的科学上网软件必定是：Shadowrocket，但是需要注册一个非国区或美区账号才能进行购买，目前是2.99美刀约20块人民币，注册美区账号和充值购买也非常简单，请参考以下两篇文章。
如何注册美区Apple ID:https://zhuanlan.zhihu.com/p/635054054
美区账号如何充值：https://zhuanlan.zhihu.com/p/636121931
