# Shadowrocket Configuration Changelog

## v1.0.0 (2026-07-13)

### Initial Release

**执行时间**: 2026-07-13 20:00
**配置文件版本**: v1.0.0

### 规则集状态检查

| 规则集 | 最后更新 | 状态 | 备注 |
|--------|----------|------|------|
| ChinaMax | 2026-07-13 | 已引用 | 核心国内直连规则 |
| ChinaIPs | 2026-07-13 | 已引用 | 中国 IP 段 |
| ChinaIPsBGP | 2026-07-13 | 已引用 | 中国 BGP 路由 |
| Lan | 2026-07-13 | 已引用 | 局域网直连 |
| Advertising | 2026-07-13 | 已引用 | 广告拦截 |
| OpenAI | 2026-07-13 | 已引用 | AI 服务代理 |
| Google | 2026-07-13 | 已引用 | 谷歌服务代理 |
| YouTube | 2026-07-13 | 已引用 | 视频流媒体代理 |
| Twitter | 2026-07-13 | 已引用 | 社交媒体代理 |
| Netflix | 2026-07-13 | 已引用 | 流媒体代理 |
| Global | 2026-07-13 | 已引用 | 全球代理兜底 |
| Proxy | 2026-07-13 | 已引用 | 代理兜底 |

### 本次变更

- 初始配置文件生成
- 基于 blackmatrix7/ios_rule_script 规则集构建
- 国内服务直连：WeChat, Tencent, Alibaba, ByteDance, Baidu, BiliBili 等 26 个规则集
- 国外服务代理：OpenAI, Claude, Google, YouTube, Netflix 等 20 个规则集
- 国内 AI 服务直连白名单：智谱、Kimi、讯飞、豆包、混元、商汤、MiniMax、零一万物、DeepSeek
- 规则优先级：LAN > REJECT > 国内直连 > 国外代理 > GEOIP,CN > FINAL

### 发布状态

- GitHub 提交: 首次提交
- Raw 链接: https://raw.githubusercontent.com/vincentZero/share/main/Shadowrocket/DirectProxy.conf
- 链接验证: 待验证

### 使用说明

1. 在 Shadowrocket 中添加远程配置
2. 填入 Raw 链接地址
3. 配置代理节点（PROXY 策略组）
4. 开启自动更新（建议每周）

### 下次检查时间

2026-07-20

---

## 规则集来源

- 所有规则集来自 [blackmatrix7/ios_rule_script](https://github.com/blackmatrix7/ios_rule_script)
- 配置维护由 Kimi Claw 自动执行
- 如有问题请联系配置维护者
