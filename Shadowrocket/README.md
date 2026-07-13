# Shadowrocket 自动配置

自动维护的 Shadowrocket 分流配置，基于 blackmatrix7/ios_rule_script 规则集构建。

## 快速开始

### 1. 订阅配置

在 Shadowrocket 中添加远程配置：

```
https://raw.githubusercontent.com/vincentZero/share/main/Shadowrocket/DirectProxy.conf
```

### 2. 配置代理节点

配置完成后，在「配置 - 策略组」中为 `PROXY` 策略组添加你的代理节点。

### 3. 开启自动更新

建议开启自动更新，默认每周检查一次规则集更新。

## 配置结构

```
优先级从高到低：
1. LAN 直连
2. 广告拦截 (REJECT)
3. 国内服务直连 (ChinaMax + 细分规则集)
4. 国内 AI 服务直连 (智谱、Kimi、讯飞、豆包、混元、DeepSeek 等)
5. 国外服务代理 (AI/流媒体/社交/搜索)
6. GEOIP,CN 直连党底
7. FINAL 代理党底
```

## 已集成规则集

### 国内直连 (27 个)
- ChinaMax / ChinaIPs / ChinaIPsBGP
- WeChat, Tencent, Alibaba, ByteDance, Baidu, BiliBili
- NetEaseMusic, IQIYI, Youku, MiguTV
- XiaoMi, JingDong, PinDuoDuo, MeiTuan, DiDi
- AMAP, BaiduMap, ChinaUnionPay, ChinaBank, ChinaStock
- ChinaTelecom, ChinaUnicom, ChinaMobile
- AlibabaCloud, TencentCloud, HuaweiCloud

### 国外代理 (20 个)
- OpenAI, Claude, Gemini, Copilot, Perplexity, Anthropic
- Google, GoogleFCM, YouTube
- Twitter, Facebook, Instagram, WhatsApp, Telegram, Reddit, Discord, Twitch, TikTok, Pinterest, LinkedIn, Medium, Substack
- Netflix, Disney, HBO, AmazonPrimeVideo, Spotify, GlobalMedia
- PayPal, Steam, Epic, Speedtest
- Global, Proxy

## 更新日志

查看 [changelog.md](changelog.md)

## 注意事项

1. 此配置不包含具体代理节点，需要你自行添加
2. DNS 设置为国内优先，避免 CDN 调度异常
3. 国内 AI 服务已手动置为直连，确保 API 调用走国内网络
4. 每次更新前会保留上一版本配置

## 规则集来源

- [blackmatrix7/ios_rule_script](https://github.com/blackmatrix7/ios_rule_script)

## 维护者

- 自动维护: Kimi Claw
- 仓库: https://github.com/vincentZero/share
