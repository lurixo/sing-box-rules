<div align="center">

[简体中文](README.md) | **English**

# 🚀 Sing-box Rules Collection

[![License](https://img.shields.io/badge/license-GPL--3.0-blue?style=flat-square)](https://github.com/lurixo/sing-box-rules/blob/main/LICENSE)
[![Last Commit](https://img.shields.io/github/last-commit/lurixo/sing-box-rules?style=flat-square)](https://github.com/lurixo/sing-box-rules/commits)
[![GitHub Stars](https://img.shields.io/github/stars/lurixo/sing-box-rules?style=flat-square)](https://github.com/lurixo/sing-box-rules)
[![GitHub Issues](https://img.shields.io/github/issues/lurixo/sing-box-rules?style=flat-square)](https://github.com/lurixo/sing-box-rules/issues)

**✨ Deeply Customized for Personal Needs | 🔄 Continuously Updated | 🎯 Precise Traffic Routing Rules**

## 🔗 Data Sources

<table>
<tr>
<th align="center">Rule Set</th>
<th align="center">Upstream Repository</th>
<th align="center">Description</th>
</tr>
<tr>
<td align="center">geosite-cn</td>
<td align="center"><a href="https://github.com/Dreista/sing-box-rule-set-cn/tree/rule-set">Dreista/sing-box-rule-set-cn</a></td>
<td align="center">Base rule set, heavily customized</td>
</tr>
<tr>
<td align="center">geosite-private</td>
<td align="center"><a href="https://github.com/MetaCubeX/meta-rules-dat/tree/sing/geo/geosite">MetaCubeX/meta-rules-dat</a></td>
<td align="center">Modified regex to support intranet domains starting with uppercase letters</td>
</tr>
<tr>
<td align="center">geosite-cryptocurrency</td>
<td align="center">Packet capture + Internet collection</td>
<td align="center">Cryptocurrency exchanges and blockchain service domains</td>
</tr>
<tr>
<td align="center">geosite-binance</td>
<td align="center">Extracted from geosite-cryptocurrency</td>
<td align="center">Binance ecosystem specific rules, a subset of geosite-cryptocurrency</td>
</tr>
<tr>
<td align="center">geoip-cn-ipv4/ipv6</td>
<td align="center"><a href="https://github.com/Dreista/sing-box-rule-set-cn/tree/rule-set">Dreista/sing-box-rule-set-cn</a></td>
<td align="center">Mainland China IP ranges</td>
</tr>
</table>

## 🗂️ Rule Set Details

### 📍 [Geosite Rule Sets](https://github.com/lurixo/sing-box-rules/tree/geosite)

| Rule Set | Description | Direct Links |
|:---:|:---:|:---:|
| **geosite-cn** | Mainland China site rules (deeply customized) | [JSON](https://github.com/lurixo/sing-box-rules/blob/geosite/geosite-cn.json) / [SRS](https://github.com/lurixo/sing-box-rules/blob/geosite/geosite-cn.srs) |
| **geosite-private** | Private domain rule set (modified) | [JSON](https://github.com/lurixo/sing-box-rules/blob/geosite/geosite-private.json) / [SRS](https://github.com/lurixo/sing-box-rules/blob/geosite/geosite-private.srs) |
| **geosite-cryptocurrency** | Cryptocurrency exchanges and blockchain services | [JSON](https://github.com/lurixo/sing-box-rules/blob/geosite/geosite-cryptocurrency.json) / [SRS](https://github.com/lurixo/sing-box-rules/blob/geosite/geosite-cryptocurrency.srs) |
| **geosite-binance** | Binance ecosystem specific rules (cryptocurrency subset) | [JSON](https://github.com/lurixo/sing-box-rules/blob/geosite/geosite-binance.json) / [SRS](https://github.com/lurixo/sing-box-rules/blob/geosite/geosite-binance.srs) |

<details>
<summary><b>View Details</b></summary>

<div align="center">
<table border="0" style="margin: 0 auto; border: none;">
<tr><td align="left" style="border: none;">

**Domains removed from geosite-cn:**

**Tech Services:**
- PikPak, Microsoft, Google, Amazon, Oracle, Steam, GitHub
- Azure, CloudFlare, Samsung, Windows, V2EX, EdgeOne

**Cryptocurrency:**
- Removed 55 keywords covering major exchanges and blockchain services such as Binance, Coinbase, Ethereum, etc. These have been organized into the geosite-cryptocurrency rule set. See [geosite-cryptocurrency.json](https://github.com/lurixo/sing-box-rules/blob/geosite/geosite-cryptocurrency.json) for details

**Bing related domains (exact match):**
- bing.com.cn, cn.bing.com, cn.bing.net, cn.mm.bing.net
- ditu.live.com, r.bing.com, th.bing.com

**Special handling:**
- Ensures all .cn suffix domains are correctly included in the rule set
- Automatically adds .cn suffix rules to cover all Chinese domains

**geosite-private modifications:**
- Modified regex to support intranet domains starting with uppercase letters

**Relationship between geosite-binance and geosite-cryptocurrency:**
- geosite-cryptocurrency covers all major cryptocurrency exchanges and blockchain services
- geosite-binance is a subset, containing only Binance and its ecosystem domains (BNBChain, BSCScan, CoinMarketCap, etc.)
- Use geosite-cryptocurrency for routing all crypto traffic; use geosite-binance if you only need Binance ecosystem routing

</td></tr>
</table>
</div>

</details>

### 📍 [GeoIP Rule Sets](https://github.com/lurixo/sing-box-rules/tree/geoip)

| Rule Set | Description | Direct Links |
|:---:|:---:|:---:|
| **geoip-cn-ipv4** | IPv4 address rules | [JSON](https://github.com/lurixo/sing-box-rules/blob/geoip/geoip-cn-ipv4.json) / [SRS](https://github.com/lurixo/sing-box-rules/blob/geoip/geoip-cn-ipv4.srs) |
| **geoip-cn-ipv6** | IPv6 address rules | [JSON](https://github.com/lurixo/sing-box-rules/blob/geoip/geoip-cn-ipv6.json) / [SRS](https://github.com/lurixo/sing-box-rules/blob/geoip/geoip-cn-ipv6.srs) |

<details>
<summary><b>View Details</b></summary>

<div align="center">
<table border="0" style="margin: 0 auto; border: none;">
<tr><td align="left" style="border: none;">

· **IPv4 address rules**: Complete mainland China IPv4 address ranges  
· **IPv6 address rules**: Supports the latest IPv6 address allocations  
· Synced with upstream repository

</td></tr>
</table>
</div>

</details>

## ⚠️ Disclaimer

<div align="center">
<table border="0" style="margin: 0 auto; border: none;">
<tr><td align="left" style="border: none;">

· This rule set is a personally customized version and may not be suitable for all use cases  
· The author assumes no responsibility for any issues caused by using this rule set

</td></tr>
</table>
</div>

## 📄 License

This project is licensed under the [GPL-3.0 License](https://github.com/lurixo/sing-box-rules/blob/main/LICENSE)

---

**🌟 If this project helps you, please give it a Star!**

Made with ❤️ by [lurixo](https://github.com/lurixo)

</div>
