# IEPL价格：按流量还是按带宽算更划算，各线路套餐价位、优惠码与预算方法一次看清

搜"IEPL 价格"的人，基本都被同一种信息差折磨过：有人说专线一个月两百块就能起步，有人说没有五千预算免谈，还有商家报价比服务器本身还贵。这两种说法其实都对，只是他们买的根本不是同一种东西。

IEPL 专线的价格差距，主要不来自品牌溢价，而来自计费方式、线路方向和带宽模式。这篇文章以 Mkcloud（mkcloud.net，2023 年成立的国人专线服务商）当前在售套餐为样本，把流量计费和独享带宽两种算法的价格拆开讲清楚，顺便给你一套能自己算预算的方法。

## 先说结论：IEPL 一个月到底多少钱

以 Mkcloud 目前公开的套餐价为准，大致分三档：

- **流量计费（共享带宽）**：入门款月付 **158～228 元**。最便宜的是深港 IX 上云互联 2TB/500Mbps 档，158 元/月；广港 IEPL 500GB/150Mbps 是 228 元/月。适合日常跨境办公、店铺后台、SSH 和 API 这类间歇性使用。
- **小带宽独享（不限流量）**：5M～20M 独享，月付 **500～1760 元**。广港 IEPL 独享 5M 是 500 元/月，沪港 IPLC 独享 5M 是 650 元/月。
- **大带宽独享**：100M 起步就到 **5800 元/月**，1G 独享在 9000～24000 元/月之间，2G 以上直奔四万。这类基本是企业级采购，量大还能议价。

所以"IEPL 很贵"和"IEPL 两百块"两种说法可以同时成立。你要是每月就传几十 GB 数据，花五千块买独享纯属浪费；反过来，要是直播推流要 200M 持续速率，两百块的共享峰值款也顶不住。

## 影响 IEPL 价格的四个变量

Mkcloud 官方知识库里有一篇专门讲专线定价的文章，口径很实在：价格由出口方向、共享峰值或独享配置、月流量、CPU/内存/硬盘以及接入条件共同决定。展开说就是四件事：

**一是线路方向和延迟。** 同样是 500GB/150Mbps 的配置，广港 IEPL（广州→香港，端内 1~2ms）卖 228 元，沪日 IPLC（上海→日本，25~28ms）也是 228 元，而沪美 IPLC（124~134ms）同档要 428 元起。物理距离和海缆成本直接反映在账单上，越远越贵，这条规律基本成立。

**二是共享还是独享。** 这是大部分人算错账的地方。共享流量款给的是峰值带宽加月流量额度，比如 200Mbps 峰值 + 1024GB/月；独享款反过来，带宽是你独占的持续速率，流量不限。沪港方向就有个很典型的对比：共享入门 200Mbps/1024GB 卖 288 元/月，独享入门 5Mbps/不限流量卖几百元。看着共享"带宽更大"，但如果你的业务是每天十几个小时持续传输，5M 独享反而更对路，因为共享峰值不保证一直跑满。

**三是流量额度。** Mkcloud 的计量型套餐按上行、下行**双向**统计流量，超量后暂停服务。这一点和很多按单边计的 VPS 不一样，实际可用量要打个对折预估。超量后可以自助购买流量重置继续用（有第三方测评提到重置价格约为原价 9 折，具体以下单页为准），也可以提交工单补差价升级套餐。

**四是 IP 和接入条件。** 好消息是，Mkcloud 现售的共享和独享套餐都给每台 VPS 分配 1 个独立入口 IP 加 1 个独立出口 IP，也就是"一进一出"双独享 IP，这对做跨境电商多店铺隔离的人价值不小。但注意两种接入限制：直连款绑定一个省份入口；IX 款（上云互联）需要你先有一台支持范围内的云厂机器（阿里云、腾讯云、百度云国内全网等）做前置，这笔云主机的钱要算进总预算。

## Mkcloud 各线路套餐价格总表

下面两张表按计费方式拆开。价格为月付原价（人民币），来自官网购物车和官方知识库，带 † 的档位数据同步自第三方对官网的整理，下单前以购物车实时标价为准。

### 流量计费类（共享带宽，按月流量选档）

| 线路（方向/端内延迟） | 套餐 | 峰值带宽 | 配置 | 月付原价 | 购买入口 |
| --- | --- | --- | --- | --- | --- |
| 深港 IX（深圳→香港，1~2ms，需云前置） | 2TB/月 | 500Mbps | 2核4G/40G | ¥158 | [ 查看深港IX套餐](https://bit.ly/MKCLoud) |
| 深港 IX（需云前置） | 5TB/月 | 1Gbps | 4核8G/40G | ¥368 † | [ 查看深港IX套餐](https://bit.ly/MKCLoud) |
| 广港 IEPL（广州→香港，1~2ms） | 500GB/月 | 150Mbps | 1核2G/20G | ¥228 | [ 看广港IEPL现价](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-sh) |
| 广港 IEPL | 1TB/月 | 200Mbps | 1核2G/20G | ¥358 | [ 看广港IEPL现价](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-sh) |
| 广港 IEPL | 2TB/月 | 300Mbps | 2核4G/40G | ¥568 | [ 看广港IEPL现价](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-sh) |
| 广港 IEPL | 4TB/月 | 300Mbps | 2核4G/40G | ¥998 | [ 看广港IEPL现价](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-sh) |
| 广港 IEPL | 6TB/月 | 500Mbps | 4核8G/60G | ¥1388 † | [ 看广港IEPL现价](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-sh) |
| 广港 IEPL | 10TB/月 | 500Mbps | 4核8G/60G | ¥2288 † | [ 看广港IEPL现价](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-sh) |
| 广港 IEPL | 20TB/月 | 1Gbps | 4核8G/60G | ¥4500 † | [ 看广港IEPL现价](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-sh) |
| 沪港 IPLC（上海→香港，21ms） | 1024GB/月 | 200Mbps | 1核2G/20G | ¥288（季付864/年付3456） | [ 查看沪港IPLC套餐](https://bit.ly/MKCLoud) |
| 沪日 IPLC（上海→日本，25~28ms） | 500GB/月 | 150Mbps | 1核2G/20G | ¥228 | [ 去看沪日IPLC套餐](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-jp-sh) |
| 沪日 IPLC | 1TB/月 | 200Mbps | 1核2G/20G | ¥358 | [ 去看沪日IPLC套餐](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-jp-sh) |
| 沪日 IPLC | 2TB/月 | 300Mbps | 2核4G/40G | ¥568 | [ 去看沪日IPLC套餐](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-jp-sh) |
| 沪日 IPLC | 4TB/月 | 300Mbps | 2核4G/40G | ¥998 | [ 去看沪日IPLC套餐](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-jp-sh) |
| 沪日 IX（上海→日本，25~28ms，需云前置） | 1TB/月 | 200Mbps | 2核4G/40G | ¥166（年付1188元/年） | [ 看沪日IX实时价](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fcloud-jp-sh) |
| 沪日 IX（需云前置） | 2TB/月 | 300Mbps | 2核4G/40G | ¥268 | [ 看沪日IX实时价](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fcloud-jp-sh) |
| 沪日 IX（需云前置） | 3TB/月 | 500Mbps | 2核4G/40G | ¥358 | [ 看沪日IX实时价](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fcloud-jp-sh) |
| 沪日 IX（需云前置） | 6TB/月 | 1Gbps | 4核8G/40G | ¥688 | [ 看沪日IX实时价](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fcloud-jp-sh) |
| 沪美 IPLC（上海→美国，124~134ms） | 1TB/月 | 200Mbps | 2核4G/40G | ¥428 | [ 查沪美IPLC月付价格](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-us-sh) |
| 沪美 IPLC | 2TB/月 | 300Mbps | 2核4G/40G | ¥698 | [ 查沪美IPLC月付价格](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-us-sh) |
| 沪美 IPLC | 4TB/月 | 300Mbps | — | ¥1258 | [ 查沪美IPLC月付价格](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-us-sh) |

### 独享带宽类（不限月流量，按持续速率计费）

| 线路 | 独享档位 | 月付原价 | 购买入口 |
| --- | --- | --- | --- |
| 广港 IEPL 独享（1~2ms，2核4G/40G 起） | 5M / 10M / 20M | ¥500 / ¥700 / ¥1320 | [ 算算独享5M多少钱](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-ex) |
| 广港 IEPL 独享 | 50M / 100M / 200M / 300M | ¥3150 / ¥5800 / ¥11600 / ¥17400 | [ 算算独享5M多少钱](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-ex) |
| 沪港 IPLC 独享（21ms，2核4G/40G 起） | 5M / 10M / 20M | ¥650 / ¥950 / ¥1760 | [ 看沪港独享档位价](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-hk-ex) |
| 沪港 IPLC 独享 | 50M / 100M | ¥4000 / ¥7500 | [ 看沪港独享档位价](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-hk-ex) |
| 沪美 IPLC 独享（124~134ms，2核4G/40G 起） | 5M / 10M / 20M | ¥800 / ¥1100 / ¥2100 | [ 查沪美独享月付](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-us-ex) |
| 沪美 IPLC 独享 | 50M / 100M | ¥5000 / ¥9000 | [ 查沪美独享月付](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-us-ex) |
| 深港 IX 独享（1~2ms，需云前置） | 88M / 100M / 200M | ¥688 / ¥1600 / ¥3000 | [ 看深港独享报价](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fcloud-hk-ex) |
| 深港 IX 独享（需云前置） | 500M / 1G / 2G / 5G | ¥6000 / ¥9000 / ¥16000 / ¥35000 | [ 看深港独享报价](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fcloud-hk-ex) |

### 大带宽与高防专线（参考价，量大可议价）

这一档面向直播出海、游戏和企业核心业务，官方知识库给的参考价如下，实际以购物车和询价为准：

| 线路 | 独享档位 | 月付参考价 |
| --- | --- | --- |
| 广东三线 IEPL 独享（电信/联通/移动三入口，含300Gbps高防） | 200M / 500M / 1G / 2G | ¥5400 / ¥12500 / ¥23000 / ¥40000 |
| 广东移动 IEPL 独享（单网入口，含300Gbps高防） | 200M / 500M / 1G / 2G | ¥3900 / ¥9000 / ¥17000 / ¥32000 |
| 福港高防 IPLC（厦门/泉州→香港，100Gbps 高防） | 200M / 500M / 1G / 2G / 5G | ¥6000 / ¥13500 / ¥24000 / ¥46000 / ¥110000 † |

> 买大带宽之前先搞清一件事：独享的是带宽，不是整条物理线路。独享套餐同样不设 SLA 赔付，想要可用性保障得单独谈定制合同。

对这一档感兴趣的，可以直接[👉 去购物车试算大带宽独享的实时报价](https://bit.ly/MKCLoud)，带宽量大的话工单里能谈。

## 计费规则里的几个坑，下单前必须知道

**双向计量。** 前面提过，计量型套餐上下行都算流量。你上传 10GB、下载 10GB，账面就是 20GB。估算月流量时按业务峰值方向翻倍算，不然月中就停机。

**共享带宽是峰值，不是承诺值。** 200Mbps 峰值的意思是最高能到 200M，不保证任何时候都跑满。有第三方测评称广港 IEPL 150Mbps 档实测能稳定跑出 130Mbps 上下，这个数字仅供参考，你的实际体验取决于本地到入口的线路。

**退款条件严格。** 官方政策是仅质量问题支持退款，而且要在工单里提交测试截图和具体问题，由商家审核判断；开通后不支持更换到其他地域。也就是说，买之前想清楚方向和档位，别指望"买来试试不合再退"。

**升降级走工单。** 升级要补差价，降级到更低价格套餐时差价不退。建议第一次买就选对档位，宁小勿大——流量不够可以 9 折重置，买大了可退不回来。

**需要实名。** IEPL 类产品需要中国身份信息实名认证，仅限个人或企业正规用途。这不是 Mkcloud 一家的要求，国内入口的专线产品基本都这样。

**默认无 SLA。** 官方明确不承诺无中断或固定故障恢复时长，对可用性有硬指标要求的企业用户，先把这一条问清楚再下单。

## 优惠码怎么用：能省多少、哪些还能用

Mkcloud 的优惠码分两类，情况不太一样：

**循环折扣码（多次活动反复出现）：**
- `MK-8.8`：全场流量计费套餐 8.8 折循环，续费也生效。第三方优惠码站标注有效期到年底，官方多轮活动页也反复沿用它，但官方口径始终是"仅在活动期内有效"，下单时以结算页实测为准。
- `MK-IEPL-WELCOME` / `MK-IPLC-WELCOME`：IEPL 和 IPLC 产品上新时的 9 折循环码，第三方测评显示长期挂在可用列表里。注意有测评提到最低配套餐可能不可用。
- `MK-7.8`：独享带宽产品首月 7.8 折，只优惠首月。

**历史活动码（别再当现价用）：** `IXCLOUD`（沪日 IX 预售 6.9 折）、`CLOUD-2T-NEW`（上云互联 2TB）、`MK-NEW`（236 元新客活动机）这些对应的活动已经结束，官方页面明确标注失效或仅限活动期。搜到有人按历史折后价报"126 元/月的深港IX"，那是活动价，现在原价 158 元。

算一下实际效果：广港 IEPL 500GB 原价 228 元，用 8.8 折是 200.64 元；如果 9 折的 IEPL 专属码能用，是 205.2 元。两个码不能叠加，选折扣深的那个就行。结算页有优惠码输入框，先[👉 去购物车把套餐加进去试算一下](https://bit.ly/MKCLoud)，码是否生效当场就能看到，比看任何攻略都准。

## 按场景算一笔账

**跨境电商运营（店铺后台、ERP、选品）：** 每月流量通常几十到两三百 GB。广港 IEPL 500GB（228 元/月）够用，人在华南的话延迟只有几毫秒，操作后台几乎感觉不到跨境。多个店铺需要环境隔离的话，每台 VPS 自带的一进一出双独享 IP 是加分项。

**日本方向业务（自建站、日本电商、游戏联机）：** 沪日 IPLC 500GB 和广港同价（228 元/月），端内 25~28ms。对日本方向的 TCP 业务来说这个延迟完全够。预算紧还可以看沪日 IX，1TB 档月付 166 元，前提是你手上有台支持的云主机做前置。

**持续传输/备份/拉流：** 别选流量款，直接上独享。5M 独享理论上每天能传约 54GB，一个月 1.6TB 上下，广港独享 5M 卖 500 元/月。流量需求大但对速率不敏感的话，共享流量款按量买反而便宜，自己按公式算：理论传输量（GB）≈ 带宽（Mbps）× 10.8 × 每天有效小时数 × 30。

**直播出海、大流量推流：** 200M 以下看广港独享（100M 档 5800 元/月），再往上广东三线/移动 IEPL 独享带 300Gbps 高防，200M 档 3900 元起，量大议价空间也大。

**美国方向：** 沪美 IPLC 共享 1TB 档 428 元/月起，独享 5M 档 800 元/月。124~134ms 的延迟做网页和 API 没问题，打游戏就别考虑了。

## 常见问题

**IEPL 和 IPLC 价格差很多吗？** 在 Mkcloud 这家，同档位价格基本一致（500GB 档都是 228 元），差别在延迟：IEPL 走以太网专线，广港方向端内 1~2ms；IPLC 是传统租用线路，沪日 25~28ms、沪美 124~134ms。选哪家贵不贵，先看你业务在哪个方向。

**两三百块的 IEPL 是不是智商税？** 不是，但它有明确边界：共享峰值带宽、月流量额度、超量暂停、无 SLA。付这个价买的是"低延迟 + 双独享 IP + 稳定路径"，不是无限速大带宽。需求错配才是真正的智商税，产品本身不是。

**出口 IP 是原生 IP 吗？** 官方明确说当前是服务器 IP，不保证原生、住宅或流媒体解锁，也不能保证平台账号零风险。做店铺运营的别把宝全押在 IP 纯净度上，自己的使用习惯同样重要。

**能开发票、能定制吗？** 官方页面提到带宽量大可议价，支持独立服务器与定制方案，SLA、路由定制这类需求走工单或联系渠道询价。

## 最后一点建议

IEPL 价格这件事，看十篇攻略不如自己算一次。三步就够：先估月流量（记得双向翻倍），再判断是突发用量还是持续传输，然后对号入座选流量款还是独享款——预算公式就出来了。

拿不准的话，最稳妥的路径是先从广港 IEPL 500GB 这种入门档试起，月付 228 元，用 `MK-8.8` 折后两百出头，跑一个月记下真实的流量和速率曲线，再决定升档还是换独享。下单入口在这：[👉 查看 Mkcloud 全线 IEPL 套餐与实时优惠](https://bit.ly/MKCLoud)。专线这东西，够用且稳，比一步到位买大的更划算。
