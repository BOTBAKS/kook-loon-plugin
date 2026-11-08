# KOOK-Splash-Block

一个面向 Loon 的 KOOK 开屏广告拦截插件，采用本地规则，不加载远程 JavaScript，也不上传任何数据。

## 一键导入

在 Loon 中添加插件地址：

`https://raw.githubusercontent.com/BOTBAKS/kook-loon-plugin/main/KOOK-Splash-Block.plugin`

## 功能

- 拦截 KOOK 自有域名中带有 `splash`、`startup`、`launch`、`advert`、`adslot`、`ad_config`、`advertisement` 的启动/开屏广告请求。
- 对 KOOK 启动配置响应删除常见广告字段，兼容广告与启动配置合并下发的版本。
- 规则只作用于 `kookapp.cn`，不会把第三方广告平台域名加入全局拦截，减少误伤其他 App。

## 使用

1. 在 Loon 中导入上面的 Raw 地址。
2. 启用插件，并允许插件添加 MitM 主机名。
3. 安装并信任 Loon CA 证书，开启 HTTPS 解密。
4. 完全退出 KOOK 后重新打开。

## 适配范围与限制

KOOK 的接口路径可能随客户端版本调整。本插件根据公开可观察到的 KOOK 域名和启动/广告路径关键词编写；当前环境没有 KOOK 真机抓包条件，因此未声称覆盖所有版本。若仍出现开屏广告，可在 Loon 的请求日志中找到对应的 KOOK 请求 URL，再把脱敏后的路径提交 Issue 以便补充规则。

## 许可证

MIT License
