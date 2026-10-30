# ChatGPT 付款 / 订阅报错大全（2026）

> **利益披露**：本仓库由 Pay2GPT（第三方 ChatGPT 代充服务，与 OpenAI 无关联）维护。本表以 OpenAI 官方帮助中心为准，优先给官方办法；代充只在官方办法都走不通时作为选项之一出现。
>
> 最后核对：2026-10-30。

## 先看这一句

付款被拒多数是**发卡行**拦的，不是 OpenAI：银行挡了网上或境外支付，或者 3D 验证没走完。OpenAI 说它一般拿不到银行给出的具体拒付原因，所以被拒两三次后，直接打电话问银行最快（[官方说明](https://help.openai.com/en/articles/7232916-why-was-my-credit-card-declined)）。同一张卡反复重试基本没用。

## 报错对照表

| 现象 / 提示 | 最可能的原因 | 怎么办 | 官方参考 |
| --- | --- | --- | --- |
| 直接被拒，银行没弹验证 | 银行拦了网上或境外支付；卡号、有效期、CVC、账单地址或邮编和银行记录对不上 | 按银行登记的信息重填（账单地址不是收货地址）；在手机银行打开网上、境外和自动扣款；问银行 | [Why was my credit card declined?](https://help.openai.com/en/articles/7232916-why-was-my-credit-card-declined) |
| “Authentication required” / “3D Secure attempt failed” / “card may be invalid or authentication may be needed” | 银行的 3D 验证（3DS / SCA）没走完 | 允许弹窗，关掉广告拦截和 VPN，用无痕窗口或换浏览器 / 设备 / 网络；完成短信或 App 确认，期间别关闭或刷新结账页；一直不弹就请银行开通 3DS | 同上 |
| 换哪张卡都被拒 | 你本人或发卡行不在 OpenAI 支持的国家和地区（中国大陆、香港不在列表里） | 查支持列表；换支持地区银行发的卡，或走 App Store / Google Play，或换别的付款途径 | [Supported countries](https://help.openai.com/en/articles/7947663-chatgpt-supported-countries) |
| 预付卡、借记卡、虚拟卡付不了 | 卡没开网上、境外或自动扣款，或不支持 3D 验证。官方只写明预付卡不能买 **API 额度** | 让发卡方开通相应功能，或换普通信用卡 | [Why was my credit card declined?](https://help.openai.com/en/articles/7232916-why-was-my-credit-card-declined) |
| 以前能扣，这次续费失败 | 卡过期、余额不足、银行新加风控，或本人 / 发卡行不在支持地区 | 清缓存和 Cookie 重试；在「设置 → 账单」核对或更换付款方式；问银行；仍不行联系 OpenAI 支持 | [Renewal payments](https://help.openai.com/en/articles/7242622-troubleshooting-chatgpt-plus-or-pro-renewal-payments) |
| “Too many subscriptions associated with this card or device. We can’t complete this purchase” | 同一张卡或同一台设备关联的订阅太多，被卡 / 设备限制拦截（**不是**银行拒付） | 用已有的合规账号；认为限制有误时联系 OpenAI 支持。买点数或重置用量解除不了这个限制 | [Card and device limits](https://help.openai.com/en/articles/20001559-understanding-card-and-device-limits-in-chatgpt) |
| 登录时提示 “Device limit reached”，或开通后过一阵被登出 | 一台设备上使用的付费账号数量超限（Go、Plus、Pro 都算） | 换登你自己的另一个合规账号；或取消受影响的订阅并申请退款（Apple 购买要找 Apple 退） | 同上 |
| 注册时提示 “unsupported country” | 当前所在地不在支持列表 | 官方没有绕过办法；查看支持列表 | [Why can't I sign up due to "unsupported country"?](https://help.openai.com/en/articles/8983035-why-cant-i-sign-up-due-to-unsupported-country) |
| iOS App 订阅按钮灰色，提示 “In-app purchases are currently unavailable. Please try again later” | 应用内购暂时不可用 | 过一会儿再试；或在网页登录同一账号看可用的购买方式 | [iOS upgrading](https://help.openai.com/en/articles/7905739-chatgpt-ios-app-upgrading-to-a-paid-subscription) |
| App 里看不到想要的套餐或币种 | App 只显示你账号可用的套餐；网页定价页的国家选择不对 | 去网页版看；在定价页底部确认国家 | 同上 |
| 已付款但套餐没显示 | 可能付到了另一个 ChatGPT 账号上 | **先别再付一次**，按 iOS 升级说明里链接的“订阅关联到另一个账号”排错文章处理 | 同上 |
| 网页和 App 各扣了一次 | 各平台分开收费，在两个平台都订了 | 在其中一个平台取消；卸载 App 不会取消订阅 | [Canceling your subscription](https://help.openai.com/en/articles/7232927-canceling-your-chatgpt-subscription) |
| 取消后钱没退 | 取消只停止之后的续费，不会自动退还已扣的钱 | 认为扣错了，按官方流程申请退款 | 同上 |
| OpenAI 礼品卡兑换失败 | OpenAI 礼品卡只能在美国、美元计费的账号上兑换，且只能用于网页，不能用于 App Store / Google Play | 不在美国的话这张卡用不了；兑换后不能转账号也不能退 | [Gift cards](https://help.openai.com/en/articles/20001491-buying-and-redeeming-openai-gift-cards) |
| 开了 VPN 还是付不了 | VPN 改变不了发卡行所在地，OpenAI 也建议银行验证时关掉 VPN | 关掉 VPN 再走 3D 验证；发卡行不在支持地区的话，怎么设置都过不了 | [Why was my credit card declined?](https://help.openai.com/en/articles/7232916-why-was-my-credit-card-declined) |

## 代充相关的“报错”

这些不是 OpenAI 的报错，是用第三方代充时常见的问题：

| 现象 | 原因 | 怎么办 |
| --- | --- | --- |
| 代充提示当前订阅没到期、开不了 | 订阅一般不能叠加 | 等当前订阅到期再开；正规平台会给退款或保留订单 |
| 代充开通后过几天会员没了 | 常见于用盗刷卡付款的低价平台，原卡主拒付后订阅被撤销 | 找平台按售后规则处理；以后避开价格远低于官方的平台 |
| 对方要密码、验证码，或让你关两步验证 | 不是正规做法 | 直接放弃；已经给了的，立刻改密码并在「设置 → 安全」退出所有设备 |

各种开通方式的对比和挑代充的注意事项，见 [pay2gpt/chatgpt-plus-guide](https://github.com/pay2gpt/chatgpt-plus-guide)。

## 官方办法都走不通时

按顺序考虑：换一张支持地区银行发的卡 → App Store / Google Play 内购 → 请海外亲友代付 → 代充。代充怎么避坑见上面的链接；Pay2GPT 是其中一家（支付宝 / 银行卡 / USDT，不要密码），说明见 [pay2gpt.com/guide/errors](https://pay2gpt.com/guide/errors?utm_source=github&utm_medium=readme&utm_campaign=errors)。如果官方哪个办法成功了，直接付给 OpenAI 更便宜。

## 更新记录

| 日期 | 内容 |
| --- | --- |
| 2026-10-30 | 首次发布，逐条对照 OpenAI 帮助中心核对 |

## English summary

A neutral table of ChatGPT payment and subscription errors (symptom / likely cause / fix), each linked to the relevant OpenAI Help Center article: bank declines, 3D Secure failures, unsupported country or card issuer, renewal failures, “Too many subscriptions associated with this card or device”, “Device limit reached”, unavailable in-app purchases, double billing across web and app stores, and US-only OpenAI gift cards. Maintained by Pay2GPT, a third-party reseller not affiliated with OpenAI; official fixes are listed first.
