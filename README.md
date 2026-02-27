<div align="center">

**简体中文** | [English](README_EN.md)

# 🚀 Sing-box Rules Collection

[![License](https://img.shields.io/badge/license-GPL--3.0-blue?style=flat-square)](https://github.com/lurixo/sing-box-rules/blob/main/LICENSE)
[![Last Commit](https://img.shields.io/github/last-commit/lurixo/sing-box-rules?style=flat-square)](https://github.com/lurixo/sing-box-rules/commits)
[![GitHub Stars](https://img.shields.io/github/stars/lurixo/sing-box-rules?style=flat-square)](https://github.com/lurixo/sing-box-rules)
[![GitHub Issues](https://img.shields.io/github/issues/lurixo/sing-box-rules?style=flat-square)](https://github.com/lurixo/sing-box-rules/issues)

**✨ 基于个人需求深度定制 | 🔄 持续更新维护 | 🎯 精准分流规则**

## 🔗 数据来源

<table>
<tr>
<th align="center">规则集</th>
<th align="center">上游仓库</th>
<th align="center">说明</th>
</tr>
<tr>
<td align="center">geosite-cn</td>
<td align="center"><a href="https://github.com/Dreista/sing-box-rule-set-cn/tree/rule-set">Dreista/sing-box-rule-set-cn</a></td>
<td align="center">基础规则集，经过大量定制修改</td>
</tr>
<tr>
<td align="center">geosite-private</td>
<td align="center"><a href="https://github.com/MetaCubeX/meta-rules-dat/tree/sing/geo/geosite">MetaCubeX/meta-rules-dat</a></td>
<td align="center">修改正则，支持匹配大写字母开头的内网域名</td>
</tr>
<tr>
<td align="center">geosite-cryptocurrency</td>
<td align="center">抓包分析 + 互联网收集</td>
<td align="center">加密货币交易所及区块链服务相关域名</td>
</tr>
<tr>
<td align="center">geosite-binance</td>
<td align="center">从 geosite-cryptocurrency 中提取</td>
<td align="center">Binance 生态专项规则，为 geosite-cryptocurrency 的子集</td>
</tr>
<tr>
<td align="center">geoip-cn-ipv4/ipv6</td>
<td align="center"><a href="https://github.com/Dreista/sing-box-rule-set-cn/tree/rule-set">Dreista/sing-box-rule-set-cn</a></td>
<td align="center">中国大陆 IP 段</td>
</tr>
</table>

## 🗂️ 规则集详情

### 📍 [Geosite 规则集](https://github.com/lurixo/sing-box-rules/tree/geosite)

| 规则集 | 说明 | 直达链接 |
|:---:|:---:|:---:|
| **geosite-cn** | 中国大陆站点规则（深度定制） | [JSON](https://github.com/lurixo/sing-box-rules/blob/geosite/geosite-cn.json) / [SRS](https://github.com/lurixo/sing-box-rules/blob/geosite/geosite-cn.srs) |
| **geosite-private** | 私有域名规则集（已修改） | [JSON](https://github.com/lurixo/sing-box-rules/blob/geosite/geosite-private.json) / [SRS](https://github.com/lurixo/sing-box-rules/blob/geosite/geosite-private.srs) |
| **geosite-cryptocurrency** | 加密货币交易所及区块链服务规则集 | [JSON](https://github.com/lurixo/sing-box-rules/blob/geosite/geosite-cryptocurrency.json) / [SRS](https://github.com/lurixo/sing-box-rules/blob/geosite/geosite-cryptocurrency.srs) |
| **geosite-binance** | Binance 生态专项规则（cryptocurrency 子集） | [JSON](https://github.com/lurixo/sing-box-rules/blob/geosite/geosite-binance.json) / [SRS](https://github.com/lurixo/sing-box-rules/blob/geosite/geosite-binance.srs) |

<details>
<summary><b>查看详情</b></summary>

<div align="center">
<table border="0" style="margin: 0 auto; border: none;">
<tr><td align="left" style="border: none;">

**geosite-cn 移除域名：**

**科技服务类：**
- PikPak、Microsoft、Google、Amazon、Oracle、Steam、GitHub
- Azure、CloudFlare、Samsung、Windows、V2EX、EdgeOne

**加密货币类：**
- 移除了涵盖 Binance、Coinbase、Ethereum 等主流交易所及区块链服务的 55 个关键词，已整理至 geosite-cryptocurrency 规则集，具体内容请查看 [geosite-cryptocurrency.json](https://github.com/lurixo/sing-box-rules/blob/geosite/geosite-cryptocurrency.json)

**Bing 相关域名（完全匹配）：**
- bing.com.cn、cn.bing.com、cn.bing.net、cn.mm.bing.net
- ditu.live.com、r.bing.com、th.bing.com

**特别处理：**
- 确保所有 .cn 后缀域名被正确包含在规则集中
- 自动添加 .cn 后缀规则以覆盖所有中国域名

**geosite-private 修改：**
- 修改正则，支持匹配大写字母开头的内网域名

**geosite-binance 与 geosite-cryptocurrency 的关系：**
- geosite-cryptocurrency 覆盖所有主流加密货币交易所及区块链服务
- geosite-binance 是其子集，仅包含 Binance 及其生态相关域名（BNBChain、BSCScan、CoinMarketCap 等）
- 如需对所有加密货币流量分流，使用 geosite-cryptocurrency；如仅需针对 Binance 生态，使用 geosite-binance

</td></tr>
</table>
</div>

</details>

### 📍 [GeoIP 规则集](https://github.com/lurixo/sing-box-rules/tree/geoip)

| 规则集 | 说明 | 直达链接 |
|:---:|:---:|:---:|
| **geoip-cn-ipv4** | IPv4 地址规则 | [JSON](https://github.com/lurixo/sing-box-rules/blob/geoip/geoip-cn-ipv4.json) / [SRS](https://github.com/lurixo/sing-box-rules/blob/geoip/geoip-cn-ipv4.srs) |
| **geoip-cn-ipv6** | IPv6 地址规则 | [JSON](https://github.com/lurixo/sing-box-rules/blob/geoip/geoip-cn-ipv6.json) / [SRS](https://github.com/lurixo/sing-box-rules/blob/geoip/geoip-cn-ipv6.srs) |

<details>
<summary><b>查看详情</b></summary>

<div align="center">
<table border="0" style="margin: 0 auto; border: none;">
<tr><td align="left" style="border: none;">

· **IPv4 地址规则**：完整的中国大陆 IPv4 地址段  
· **IPv6 地址规则**：支持最新的 IPv6 地址分配  
· 保持与上游仓库同步

</td></tr>
</table>
</div>

</details>

## ⚠️ 免责声明

<div align="center">
<table border="0" style="margin: 0 auto; border: none;">
<tr><td align="left" style="border: none;">

· 本规则集为个人定制版本，可能不完全适合所有使用场景  
· 本人不对使用本规则集造成的任何问题负责

</td></tr>
</table>
</div>

## 📄 许可证

本项目采用 [GPL-3.0 License](https://github.com/lurixo/sing-box-rules/blob/main/LICENSE) 开源协议

---

**🌟 如果这个项目对你有帮助，请给个 Star！**

Made with ❤️ by [lurixo](https://github.com/lurixo)

</div>
