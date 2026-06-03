# 狗骨酒馆 iOS 版（unsigned IPA 项目）

这是把 Android 版核心功能迁移到 iOS 的 SwiftUI + WKWebView 项目。

## 已保留

- 狗洞入口选择
- 上次使用入口记录
- WKWebView 打开酒馆网页
- 换狗洞
- 重置酒馆：清理 WKWebView Cookie、缓存、网页数据
- 小说化阅读器：导入 `.jsonl` / `.json` / `.txt`
- 复制小说文本
- 导出小说文本

## 已删除

- 缓存状态
- 小狗加速器提示
- 缓存命中率
- 缓存目录
- 启动清缓存进度弹窗
- Android 悬浮球
- 电池白名单
- 腾讯 X5
- Android 通知栏控制

## 生成 unsigned IPA

1. 新建 GitHub 仓库。
2. 把本目录所有文件上传到仓库根目录。
3. 打开仓库的 Actions。
4. 运行 `Build unsigned IPA` workflow。
5. 运行完成后，在 Artifacts 下载 `DogBoneTavern-unsigned-ipa`。
6. 你拿这个 unsigned IPA 去签名。

## 注意

`Info.plist` 里已经打开 `NSAllowsArbitraryLoads`，因为你当前狗洞入口是 `http://`，不是 `https://`。

Bundle ID 默认是：

```text
com.xixijiuguan.dogbonetavern
```

如果你的签名工具要求固定 Bundle ID，可以在 Xcode 项目 Build Settings 或 `project.pbxproj` 里改 `PRODUCT_BUNDLE_IDENTIFIER`。
