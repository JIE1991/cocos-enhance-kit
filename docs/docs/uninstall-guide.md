---
sidebar_position: 5
---

# 卸载指南

虽然服务包没有对项目有侵入性修改，但这种操作还是有风险的，毕竟这就像要将引擎降级一样。

所以我们提供两种卸载方式仅供参考：

:::tip 提示

即使是手动安装的服务包，依然可以通过引擎扩展进行卸载，反之亦然。

:::

## 使用引擎扩展卸载 

TODO

## 手动卸载

### 1.代码依赖

如果你的是 TypeScript 项目，则可以先删除 `creator-sp.d.ts` 文件，让 TypeScript 对使用了服务包接口的代码发出报错。

这一步我们要确保所有代码都不再依赖服务包的特性。

### 2.资源依赖

服务包提供了一些内置资源，像是多纹理 Effect 着色器资源，你可以通过查找引用将资源的引用全部移除。

### 3.恢复自定义引擎与删除扩展

打开 Cocos Creator 菜单的项目 - 项目设置 - 自定义引擎，勾选使用内置引擎。

将服务包相关的扩展（比如 `service-pack-support` 目录）删除。