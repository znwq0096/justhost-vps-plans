# justhost 官网是哪个：三个同名 JustHost 怎么分辨？VPS 从 $1.99 起，套餐、IPv4 与备份限制一次说清（附全套餐价格表）

搜 justhost 官网，跳出来的结果里至少有三个叫 JustHost 的站点，卖的东西差得很远。

一类是本文要讲的这家：justhost.asia 上卖 KVM 虚拟化的 VPS/VDS，套餐页标题就是“VPS from $1.99”，页面自述从 2005 年运营至今，机房位置标称 80 个、覆盖 41 个国家。另外两个同名的都在美国共享主机那一侧——一个首页打着首期 $3.95/月、原价 $9.49/月，送域名、cPanel、30 天退款；另一个已经挂上 Bluehost 的合作页面，主推 Bluehost Cloud 托管 WordPress 和网站设计服务。名字一样，产品线、计费方式、目标用户完全不是一回事。

本文只讲第一家。下面把套餐价格、IPv4 到底该不该单买、官方写在 FAQ 里但很少被提起的限制，以及不同预算该选哪一档，逐条讲清楚。

> **一句话结论**：只跑轻量任务、不需要 IPv4，Sirius IPv6 的年付价 $2.88/月是这家最便宜的可用档；要建站、一定要 IPv4，就直接买双栈版，别买 IPv6 版再补 IP，单买一个 IPv4 是 $3.31/月，补完比双栈还贵。想直接看当前全部档位和实时价格，从这里进：
> 👉 [查看 JustHost VPS 全部套餐与 12 个月付价格](https://justhost.asia/en/services/vps?ref=196392)

## 先确认你找的是哪一个 JustHost

三家同名站点的区别，一张表能说清：

| 你看到的站点 | 主营 | 当前价格口径 | 谁该去 |
| --- | --- | --- | --- |
| justhost.asia 上的 JustHost | KVM VPS / VDS，SSH 自管 | 套餐页标“VPS from $1.99”，另有 12 个月付 -20% 折扣 | 要一台能自己装环境、随时换机房的服务器 |
| 美国老牌共享主机那家 | 共享主机、建站套装 | 首期 $3.95/月，原价 $9.49/月，续费按原价 | 完全不想碰命令行，只要一个能挂 WordPress 的空间 |
| 已并入 Bluehost 体系的那家 | Bluehost Cloud 托管 WordPress、网站设计 | 未在本文核验范围 | 要托管型 WordPress，不介意绑定 Bluehost 生态 |

共享主机和 VPS 的分界线在权限。共享主机给你一个控制面板和网站目录，装什么、用什么版本、开哪个端口都由商家定；VPS 给你 root 和一块独立分配的 CPU、内存、磁盘，装什么自己说了算，代价是系统、安全、备份全归你管。搜“justhost 官网”的人里，有一部分其实只想要前者，那就别在这家买 VPS，买了也用不上。

## JustHost 全部套餐与价格

这家 VPS 全部以美元计价。套餐页给两个数字：左边是月付标价，右边是标注 -20% 的 12 个月付折后价。年付折扣有门槛——New Star、Double Star、Bright Star 这三档特惠明确写着“订购 3 个月或以上”才能用年付价，其余双栈和 IPv6 档位没有这条限制。

先算一下年付到底省多少。New Star 月付 $3.81，年付折后 $3.05，每月省 $0.76，一年多付一次 $36.60 换全年，总共省 $9.12。金额不大，但如果这台机器你确定要用满一年，没有理由按月付。

### 特惠组（页面未标注 IPv4 地址）

| 套餐 | CPU · 内存 · 磁盘 | 端口（等效月流量） | 12 个月付折后价 | 订购 |
| --- | --- | --- | --- | --- |
| VPS Promo | 1 核 · 512 MB · 5 GB NVMe | 10 Mbps（4+ TB） | $1.99（页面未给折后价） | [ 选这档](https://justhost.asia/en/services/vps/tariffs/promo-c1r512nvme?ref=196392) |
| New Star | 1 核 · 1024 MB · 10 GB NVMe | 100 Mbps（31+ TB） | $3.05（月付 $3.81） | [ 选这档](https://justhost.asia/en/services/vps/tariffs/new-star-c1r1024nvme?ref=196392) |
| Double Star | 2 核 · 2048 MB · 20 GB NVMe | 200 Mbps（62+ TB） | $5.67（月付 $7.08） | [ 选这档](https://justhost.asia/en/services/vps/tariffs/double-star-c2r2048nvme?ref=196392) |
| Bright Star | 4 核 · 4096 MB · 30 GB NVMe | 300 Mbps（93+ TB） | $7.84（月付 $9.80） | [ 选这档](https://justhost.asia/en/services/vps/tariffs/bright-star-c4r4096nvme?ref=196392) |

Promo 那档的 $1.99 就是官网“VPS from $1.99”的来源。它的配置也确实是入门级：512 MB 内存、5 GB 磁盘、10 Mbps 端口，页面没给它标年付折后价。这台机器适合放个监控脚本、跑个定时任务，或者当跳板，别指望它扛网站。

### IPv4 + IPv6 双栈组

| 套餐 | CPU · 内存 · 磁盘 | 端口（等效月流量） | 12 个月付折后价 | 订购 |
| --- | --- | --- | --- | --- |
| Sirius | 1 核 · 1024 MB · 20 GB | 300 Mbps（93+ TB） | $3.88（月付 $4.85） | [ 选这档](https://justhost.asia/en/services/vps/tariffs/sirius?ref=196392) |
| Arcturus | 1 核 · 2048 MB · 30 GB | 300 Mbps（93+ TB） | $5.53（月付 $6.92） | [ 选这档](https://justhost.asia/en/services/vps/tariffs/arcturus?ref=196392) |
| Alpha Centauri | 2 核 · 2048 MB · 40 GB | 400 Mbps（124+ TB） | $7.19（月付 $8.99） | [ 选这档](https://justhost.asia/en/services/vps/tariffs/alpha_centauri?ref=196392) |
| Vega | 2 核 · 4096 MB · 80 GB | 500 Mbps（155+ TB） | $10.75（月付 $13.44） | [ 选这档](https://justhost.asia/en/services/vps/tariffs/vega?ref=196392) |
| Capella | 4 核 · 4096 MB · 120 GB | 750 Mbps（232+ TB） | $14.64（月付 $18.30） | [ 选这档](https://justhost.asia/en/services/vps/tariffs/capella?ref=196392) |
| Rigel | 4 核 · 8192 MB · 200 GB | 750 Mbps（232+ TB） | $22.35（月付 $27.94） | [ 选这档](https://justhost.asia/en/services/vps/tariffs/rigel?ref=196392) |
| Antares | 5 核 · 8192 MB · 300 GB | 750 Mbps（232+ TB） | $26.49（月付 $33.12） | [ 选这档](https://justhost.asia/en/services/vps?ref=196392) |
| Betelgeuse | 6 核 · 12288 MB · 400 GB | 750 Mbps（232+ TB） | $36.43（月付 $45.54） | [ 选这档](https://justhost.asia/en/services/vps?ref=196392) |
| Spica | 8 核 · 16384 MB · 500 GB | 750 Mbps（232+ TB） | $48.85（月付 $61.06） | [ 选这档](https://justhost.asia/en/services/vps?ref=196392) |
| Altair | 8 核 · 24576 MB · 600 GB | 750 Mbps（232+ TB） | $65.41（月付 $81.76） | [ 选这档](https://justhost.asia/en/services/vps?ref=196392) |
| Aldebaran | 8 核 · 32768 MB · 700 GB | 750 Mbps（232+ TB） | $98.53（月付 $123.16） | [ 选这档](https://justhost.asia/en/services/vps?ref=196392) |
| Procyon | 12 核 · 32768 MB · 1000 GB | 1000 Mbps（309+ TB） | $131.65（月付 $164.56） | [ 选这档](https://justhost.asia/en/services/vps?ref=196392) |

### IPv6 单栈组

| 套餐 | CPU · 内存 · 磁盘 | 12 个月付折后价 | 订购 |
| --- | --- | --- | --- |
| Sirius IPv6 | 1 核 · 1024 MB · 20 GB | $2.88（月付 $3.61） | [ 选这档](https://justhost.asia/en/services/vps?ref=196392) |
| Arcturus IPv6 | 1 核 · 2048 MB · 30 GB | $3.88（月付 $4.85） | [ 选这档](https://justhost.asia/en/services/vps?ref=196392) |
| Alpha Centauri IPv6 | 2 核 · 2048 MB · 40 GB | $5.53（月付 $6.92） | [ 选这档](https://justhost.asia/en/services/vps?ref=196392) |
| Vega IPv6 | 2 核 · 4096 MB · 80 GB | $8.27（月付 $10.33） | [ 选这档](https://justhost.asia/en/services/vps?ref=196392) |
| Capella IPv6 | 4 核 · 4096 MB · 120 GB | $10.75（月付 $13.44） | [ 选这档](https://justhost.asia/en/services/vps?ref=196392) |
| Rigel IPv6 | 4 核 · 8192 MB · 200 GB | $16.55（月付 $20.68） | [ 选这档](https://justhost.asia/en/services/vps?ref=196392) |
| Antares IPv6 | 5 核 · 8192 MB · 300 GB | $19.60（月付 $24.50） | [ 选这档](https://justhost.asia/en/services/vps?ref=196392) |
| Betelgeuse IPv6 | 6 核 · 12288 MB · 400 GB | $26.95（月付 $33.69） | [ 选这档](https://justhost.asia/en/services/vps?ref=196392) |
| Spica IPv6 | 8 核 · 16384 MB · 500 GB | $41.39（月付 $51.73） | [ 选这档](https://justhost.asia/en/services/vps?ref=196392) |
| Altair IPv6 | 8 核 · 24576 MB · 600 GB | $57.13（月付 $71.41） | [ 选这档](https://justhost.asia/en/services/vps?ref=196392) |
| Aldebaran IPv6 | 8 核 · 32768 MB · 700 GB | $82.79（月付 $103.48） | [ 选这档](https://justhost.asia/en/services/vps?ref=196392) |
| Procyon IPv6 | 12 核 · 32768 MB · 1000 GB | $107.63（月付 $134.53） | [ 选这档](https://justhost.asia/en/services/vps?ref=196392) |

三张表的价格整理自官网套餐页展示，单位美元，括号内为月付标价。汇率、活动与页面版本都会让结算页金额和表格有出入，下单前请以结算页实际扣款金额为准。

## IPv4 要不要单买：算完这笔账就清楚了

每个 VPS 都送免费 IPv6 地址。IPv4 是单独计费的，官方附加服务价目表写着 $3.31/月。这就产生一个很多人踩过的坑：先买了便宜的 IPv6 版，发现某些服务连不上，再补一个 IPv4。

拿 Sirius 算。双栈版年付 $3.88/月。IPv6 版年付 $2.88/月，加一个 IPv4 是 $2.88 + $3.31 = $6.19/月。**每月多付 $2.31，一年多付 $27.72，换来的还是同一台 1 核 1 GB 的机器。** 按标价算也一样：$3.61 + $3.31 = $6.92，比双栈的 $4.85 贵 $2.07。

结论很简单：确定需要 IPv4，就直接买双栈版，别绕这一圈。IPv6 单栈只对一种情况有意义——你确实只需要 IPv6，比如纯 IPv6 的测试环境、给已有双栈机器做备份节点、或者跑只对外提供 IPv6 服务的程序。

特惠组的情况稍微复杂。Promo 和三个 Star 档位的页面只标了免费 IPv6，没标 IPv4 地址，要用 IPv4 得按 $3.31/月 加购。以 Bright Star 为例：4 核 4 GB、年付 $7.84，加 IPv4 后是 $11.15/月。同为 4 核 4 GB 的 Capella 双栈版年付 $14.64，比它贵 $3.49，但磁盘从 30 GB 变成 120 GB、端口从 300 Mbps 变成 750 Mbps，还自带双栈。

所以这条规则可以写死：只想要 4 核 4 GB 加一个 IPv4，Bright Star 加购更便宜；磁盘和带宽也想要，直接上 Capella，多出的 $3.49 买的是 90 GB NVMe 和 2.5 倍端口。

👉 [直接开通带 IPv4 的双栈 Sirius（$3.88/月，12 个月付）](https://justhost.asia/en/services/vps/tariffs/sirius?ref=196392)

## 便宜在哪：不限流量、随时换机房、免费迁移

这家的定价逻辑和多数 VPS 商不一样：**不按流量收费，按磁盘大小收费。** 官方 FAQ 的原话是“你只为磁盘空间付费，每个套餐都包含不限流量”。端口是 fair-share（公平共享），页面给了等效值：100 Mbps 约等于每月 31+ TB，300 Mbps 约 93+ TB，1 Gbps 约 309+ TB。只要不是持续跑满端口，正常建站、跑 API、做下载镜像都用不到这个上限。

换机房是这家比较少见的一项。官网写着 80 个机房位置、41 个国家，客户中心里可以随时切换 VPS 所在地。对做跨境业务或者需要测试不同地区访问质量的人来说，这意味着一台机器能当几台用，不用为了换个地区重新买、重新配环境。IP 也能在客户中心随时更换。

其余几项也写在“所有套餐均包含”里：

- 免费 IPv6 地址，每个 VPS 都有
- 内置 DDoS 防护，官方描述是流量监控加攻击拦截的多层方案
- 免费迁移，官方会搬文件、数据库和服务器配置，你只需要提供现有主机的访问权限
- 随时升配，加 CPU 核、加内存、加磁盘都不用迁数据，停机时间很短
- SSH 直连，可以 git、跑 bash 脚本
- 24/7 技术支持
- 随时取消

迁移这项对已经在别处有站点的人价值最高。换 VPS 最烦的从来不是买，是把站点搬过去不出错。

## 坑在哪：官方不提供自动备份

这条必须单独拎出来说，因为它是官方 FAQ 里明写的：

> “No, we don't offer automatic backups. Instead, set up your own backup server and keep copies on a separate server for extra reliability.”

翻译过来就是：不提供自动备份，请自建备份服务器，把副本放在另一台机器上。

这不是小事。市面上不少 VPS 商会在面板里塞一个快照按钮，用不用得上另说，至少有。这家没有，快照、定时备份、一键回滚全部要你自己搭：另一台 VPS 上跑 rsync 或 restic，或者用对象存储存定时导出的数据库和文件。多出来的成本是一台备份机的钱，最少也要 $2.88/月，或者几美元的存储费。

如果你运维过服务器，这只是多写一个 cron 的事。如果你没碰过服务器，又打算把唯一一份生产数据放在上面，这条建议当成一票否决：要么先学会做备份，要么换成带自动备份的方案。

官方提供付费代管，系统管理服务按 $9.16/小时计费，适合临时请人处理具体问题，不适合当成长期备份方案。

👉 [先看一眼套餐总览页，确认配置和价格再决定](https://justhost.asia/en/services/vps?ref=196392)

## 附加服务价格：低价套餐的真实月成本

| 项目 | 价格 |
| --- | --- |
| 系统管理服务 | $9.16/小时 |
| 单独 IPv4 地址 | $3.31/月 |
| 增加 10 Mbps 带宽 | $2.50/月 |
| 独享 1 Gbps 带宽 | $333.33/月 |

前三项都是常见需求，加起来会明显改变真实月成本。一年下来，$3.05 的 New Star 加上 IPv4 就是 $6.36/月，接近翻倍。最后那项独享千兆是给企业级流量准备的，个人用户基本用不上，列在这里只是提醒别在配置器里点错。

## 按场景选：哪一档够用，哪一档多余

**只跑脚本、测试、临时环境，不介意只有 IPv6** → Promo $1.99 或 New Star $3.05。Promo 的 512 MB 内存和 5 GB 磁盘装完系统剩不下多少，能跑的东西很有限；多花 $1.06 上 New Star，内存翻倍、磁盘翻倍、端口从 10 Mbps 变 100 Mbps，这笔升级值。

**建站、要 IPv4、流量不大** → Sirius $3.88。1 核 1 GB、20 GB 磁盘、300 Mbps 端口，跑一个静态站或轻量 WordPress 加缓存够用。

**WordPress 加数据库、或者两三个小站** → Arcturus $5.53 或 Alpha Centauri $7.19。2 GB 内存是跑数据库的底线，Alpha Centauri 的双核在并发上来时比单核从容。

**多站点、需要更大磁盘和高带宽** → Vega $10.75 或 Capella $14.64。Capella 的 120 GB 磁盘和 750 Mbps 端口是这家里性价比变化最明显的一档。

**跑数据库、电商、CI 构建** → Rigel $22.35 起步，8 GB 内存。

**Betelgeuse 及以上（$36.43 到 $131.65）** → 单机跑重负载、要替代一台独立服务器时才考虑。绝大多数个人和小团队用不到这个区间，多花的钱不如拿去买备份机。

## 常见问题

**justhost 官网到底是哪个？**
取决于你要什么。要 KVM VPS，是 justhost.asia 这家，套餐页写“VPS from $1.99”，页面自述 2005 年运营至今。要共享主机和建站套装，是美国那家首期 $3.95/月的。要 Bluehost Cloud 托管 WordPress，是已经并入 Bluehost 体系的那个。三家产品不互通，账号也不通用。

**一定要买 IPv4 吗？**
看你的服务面向谁。纯 IPv6 环境、测试用途、备份节点不需要；面向普通用户建站、要接第三方 API、要收邮件，基本上还是得有 IPv4。需要就直接选双栈版，别买 IPv6 版再补，补完更贵。

**能退款吗？**
官网只写了随时取消（Easy cancellation），没有公开列出售后多少天内可退。这一点和其他主打“30 天退款”的共享主机不同，下单前建议先问客服确认当前政策，别按别家的规则想当然。

**送自动备份吗？**
不送，官方 FAQ 明确说明，并建议自建备份服务器。

**能换机房、换 IP 吗？**
能，都在客户中心操作，随时可换，不需要重新购买。

**年付比月付便宜多少？**
套餐页标 -20%，折后价对应 12 个月付。New Star、Double Star、Bright Star 三档特惠还需要满足“订购 3 个月或以上”才适用。

## 下单前确认两件事

第一件，结算页的最终金额和计费周期。-20% 只对 12 个月付生效，那三档特惠还多一条 3 个月起订的限制，页面上标的月付价和实际扣款是两回事。

第二件，备份放哪。官方不提供自动备份，这是买之前就要想好的事，不是买完再说。

其余按预算对号入座：只缺一台便宜机器，Promo 或 New Star；要 IPv4 建站，Sirius 起；4 GB 内存，Vega 或 Capella；8 GB 以上，Rigel 起。中间那些 $36 以上的档位，除非你明确知道自己要那么多核和内存，否则用不上。

👉 [前往 JustHost 套餐总览页，按当前价格选一档](https://justhost.asia/en/services/vps?ref=196392)
