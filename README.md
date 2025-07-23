<div align="center">

# 📦 sing-box 自用规则集导航

[![License](https://img.shields.io/github/license/lurixo/sing-box-rules)](LICENSE)
[![Last Commit](https://img.shields.io/github/last-commit/lurixo/sing-box-rules)](https://github.com/lurixo/sing-box-rules/commits)
[![GitHub Stars](https://img.shields.io/github/stars/lurixo/sing-box-rules?style=social)](https://github.com/lurixo/sing-box-rules)

_✨ 基于个人需求定制的 sing-box 分流规则集 ✨_

</div>

---

## 📋 简介

本仓库包含两个针对 sing-box 优化的规则子集，基于上游仓库并根据实际使用需求进行了大量个性化修改。

## 🔗 规则集导航

<table>
<tr>
<td width="50%">

### 🌐 [Geosite 分支](https://github.com/lurixo/sing-box-rules/tree/geosite)
**基于域名的分流规则**

经过大幅修改的域名规则集，更符合实际使用需求。

[查看 Geosite 规则 →](https://github.com/lurixo/sing-box-rules/tree/geosite/geosite)

</td>
<td width="50%">

### 📡 [GeoIP 分支](https://github.com/lurixo/sing-box-rules/tree/geoip)
**基于 IP 地址的分流规则**

包含最新的中国大陆 IP 地址段，支持 IPv4 和 IPv6。

[查看 GeoIP 规则 →](https://github.com/lurixo/sing-box-rules/tree/geoip/geoip)

</td>
</tr>
</table>

## 📊 规则集详情

### 数据来源

规则集基于上游仓库 [Dreista/sing-box-rule-set-cn](https://github.com/Dreista/sing-box-rule-set-cn/tree/rule-set)，并根据个人使用需求进行了修改。

### 🛠️ 主要修改内容

#### **geosite-cn 规则集**（大幅修改）

为了让规则集更符合实际使用需求，移除了以下类型的域名：

| 删除内容 | 原因说明 |
|---------|---------|
| **PikPak** | PikPak 很早就明确表示不对大陆用户提供服务，已多次向上游反馈但未修改 |
| **微软域名** | 主要为了阻止 Bing 搜索的恶意重定向行为 |
| **谷歌域名** | 众所周知的原因，不需要包含在国内规则中 |
| **Steam** | 游戏平台，不应归类为国内服务 |
| **GitHub** | 开发者平台，需要良好的国际访问 |
| **其他域名** | 包括 Binance、Azure、CloudFlare、Samsung 等不适合的域名 |

这些修改确保了规则集的精准性，避免了错误的流量分流。

#### **geoip-cn 规则集**（基本未修改）

- 保持与上游同步
- 仅更新版本号以兼容 sing-box

## 📁 文件说明

| 文件名 | 格式 | 说明 |
|--------|------|------|
| `geosite-cn.json` | JSON | 可读的域名规则集 |
| `geosite-cn.srs` | 二进制 | 编译后的高性能格式 |
| `geoip-cn-ipv4.json` | JSON | IPv4 地址段规则 |
| `geoip-cn-ipv4.srs` | 二进制 | 编译后的 IPv4 规则 |
| `geoip-cn-ipv6.json` | JSON | IPv6 地址段规则 |
| `geoip-cn-ipv6.srs` | 二进制 | 编译后的 IPv6 规则 |

## ⚠️ 使用说明

- 本规则集为个人定制版本，可能不适合所有人
- 如需原版规则集，请访问上游仓库
- 规则集会不定期更新，建议定期检查

---

<div align="center">
<sub>根据个人需求定制，仅供参考使用</sub>
</div>
