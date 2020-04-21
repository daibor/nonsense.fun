# 关于

这是一个基于 [LeanCloud](https://leancloud.com) 搭建的没有评论、点赞、阅读量干扰的说话空间。

*使用者应当在符合法律规定且不伤害他人的框架内表达，并为个人言论负责。*

## 对抗

1. 平台严格的审查机制；
2. 商业化产品基于流量的社交激励功能干扰（赞、评、转）；
3. 中文互联网世界里部分用户和言论对「表达」的干扰；

## 鼓励

1. 珍惜每次表达欲，忽略流量价值、他人的赞美或批评等一切与表达无关的因素，自在表达、专注表达；
2. 通过表达推动思考，进而进行更有价值的表达；

## 一些作品

- 本人的「[b言b语](https://bb.daibor.com)」
- Xu Lu 的「[废话胶囊](https://bb.lynnislu.com/)」
- Vio 的「[生活碎片](https://vio1331.github.io/)」
- [熊某人的BBtime](https://wangyr55.github.io/)
- [蹲坑沉思](https://dashlin.github.io/mythought/)
- [不吐不快](http://blog.zackzhou.com/thread/)
- [狂人日记](https://bb.elizen.me/)
- etc…

# 使用

你需要在 LeanCloud 后台创建一个名为 `content` 的 Class ，并在其中创建一个名为 `content` 的列。将 `AppID` 、`AppKey` 编辑入 `index.html` 注释提示处。然后将该文件上传至例如 `github.io` 之类 Web 服务器。

*详细配置过程请参考少数派文章[《保卫表达：用后端 BaaS 快速搭建专属无点赞评论版微博——b言b语》](https://sspai.com/post/60024)*

## 文件说明

- `index.html` 为基础版本，适用于单人使用；
- `lovers.html` 为多人版本，可用于情侣使用；
  - 还需要在 LeanCloud 后台创建一个 `Number` 类型，名为「type」的列；
  - 简单更改下文发送脚本，同样新增 `type` 字段，并设置为 0-n 的数字；

## 发送脚本

| 平台    | 支持自定义 HTTP 的应用                                       | 模板地址                                                     |
| ------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Windows | [Quicker](https://www.getquicker.net/)（可直接使用）         | [点击安装](https://getquicker.net/sharedaction?code=eeb80278-5f53-4b0d-d333-08d7e0dd26a9) |
| macOS   | 没有使用经验，欢迎评论补充                                   | 无，欢迎评论补充                                             |
| iOS     | 快捷指令（可直接使用）                                       | [点击安装](https://www.icloud.com/shortcuts/3cfcbc36a6a24e0a8721bfeef8dfc6cf) |
| Android | [Tasker](https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm&hl=en_US) | 无，欢迎评论补充                                             |

也可以查阅 LeanCloud [文档](https://console.leancloud.app/docs/rest_api.html#hash1094926014)使用任意能发送 HTTP 请求的工具发送数据；