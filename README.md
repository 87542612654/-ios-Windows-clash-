# 代理分流规则（黑名单模式）

精准海外域名走代理 / 精准国内域名直连 / 未知域名走国内，附带广告拦截。
两个文件仅含规则，不含任何节点、订阅链接或账号信息，可安全公开。

## 文件

| 文件 | 适用客户端 | 内容 |
|---|---|---|
| shadowrocket_public.conf | Shadowrocket (iOS) | 完整配置：General + 规则 + Rewrite + MITM |
| clash_public_rules.yaml | Clash / Mihomo (Clash Verge Rev、Clash Meta for Android、FlClash 等) | 仅 rules 段 |

## 规则特点

- 国内域名直连，微信/支付宝/Apple/12306 等关键 App 域名强制直连，避免广告规则误伤
- 海外域名按域名精准匹配走代理（Google/YouTube/Telegram/OpenAI/Netflix 等）
- 广告拦截：2.4 万余条 REJECT，多源交叉验证，默认不启用 MITM
- 兜底为直连（黑名单模式），未命中规则一律走国内

## 用法

**Shadowrocket**：用「用 Shadowrocket 打开」导入 conf，或订阅该文件的 raw 链接；自行添加节点后规则自动生效（PROXY 走当前选中的节点）。

**Clash / Mihomo**：把 clash_public_rules.yaml 的 rules 段粘贴到你自己的配置里；若你的代理组不叫 PROXY，全局替换成你的组名（如「节点选择」）。

## 来源

GMOogway/shadowrocket-rules、blackmatrix7/ios_rule_script、iab0x00/ProxyRules、LOWERTOP/lazy_group.conf。
