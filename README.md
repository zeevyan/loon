# loon

自用 Loon 配置仓库 —— 插件、脚本与订阅地址。

## 目录

| 文件 | 说明 | 类型 |
| --- | --- | --- |
| [`Talkatone-AdBlock.plugin`](Talkatone-AdBlock.plugin) | Talkatone 去广告 | 插件（纯 Rule） |
| [`net-lsp-x.lpx`](net-lsp-x.lpx) | 网络信息 𝕏 | 插件（脚本型） |
| [`net-lsp-x.js`](net-lsp-x.js) | 网络信息 𝕏 对应脚本 | 脚本 |

## 订阅地址

### Talkatone 去广告

拦截 Talkatone（`im.talkme.talkmeim`）内的广告与广告竞价流量：
AdMob / InMobi / Smadex / Smaato / Fyber(InnerActive) / PubMatic /
Amazon APS / PubNative / MobileFuse / Bidswitch 等。

```
https://raw.githubusercontent.com/zeevyan/loon/main/Talkatone-AdBlock.plugin
```

- 纯 `[Rule]` 域名拦截，**不需要 Mitm，不需要装证书**，不依赖任何脚本。
- ⚠️ 副作用：Talkatone 的「看广告领免费分钟数 / 解锁奖励」会一并失效。

### 网络信息 𝕏

显示当前网络、入口节点与落地节点的运营商信息；节点域名可用指定 DNS 解析。

```
https://raw.githubusercontent.com/zeevyan/loon/main/net-lsp-x.lpx
```

- 脚本型插件，长按节点 / 策略组触发。
- `net-lsp-x.lpx` 内 `script-path=net-lsp-x.js` 为**相对路径**，两个文件必须保持同目录
  —— 本仓库已满足，请勿单独移动其中一个。
- 不需要 `[Mitm]` / `[Rewrite]`。

## 添加方式

Loon → 配置 → 插件 → 右上角 `+` → 粘贴上面对应的订阅地址。

## 说明

- 所有订阅地址均指向本仓库 `main` 分支的 raw 文件，改动后无需改地址。
- 若自建加速，把 `raw.githubusercontent.com` 替换为对应域名即可。
