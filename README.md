

# 关于

这是一个基于 [LeanCloud](https://leancloud.app/) 搭建的没有评论、点赞、阅读量干扰的说话空间。

**使用者应当在符合法律规定且不伤害他人的框架内表达，并为个人言论负责。*

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
- [熊某人的BBtime](https://wangyurui.cn/)
- [蹲坑沉思](https://dashlin.github.io/mythought/)
- [不吐不快](http://blog.zackzhou.com/thread/)
- [狂人日记](https://bb.elizen.me/)
- [力言堂](http://weibo.litalk.net/)
- 木木木木木的「[b言b语](https://immmmm.com/bb/)」
- [x言x语](https://chiperman.github.io/JustBB/)
- JustSong 的「 [胡言乱语](https://nonsense.justsong.cn/)」
- etc…



## 感谢

[Jimlee2002](https://github.com/jimlee2002) 为 Android 平台制作的 Tasker [脚本](https://github.com/jimlee2002/nonsense.fun_tasker)；

[SoSo](https://sspai.com/u/0y3pn1ih/updates) 为 Android 平台提供的 Termux 解决方案（见[少数派教程](https://sspai.com/post/60024)评论区）；

[SKYue](https://www.skyue.com/) 为 Mac OS 平台提供的 Python + 命令行[解决方案及教程](https://www.skyue.com/blog/20042614.html)；

[xwlearn](https://xwlearn.com/) 为 Mac OS 平台提供的 [uTools](https://www.u.tools/) 快捷命令[解决方案及教程](https://xwlearn.com/howto-graciously-bb-in-mac/)；

# 使用

你需要在 LeanCloud 后台创建一个名为 `content` 的 Class ，并在其中创建一个名为 `content` 的列。将 `AppID` 、`AppKey` 编辑入 `index.html` 注释提示处。然后将该文件上传至例如 `github.io` 之类 Web 服务器。

*详细配置过程请参考少数派文章[《保卫表达：用后端 BaaS 快速搭建专属无点赞评论版微博——b言b语》](https://sspai.com/post/60024)*

## 文件说明

- `index.html` 为基础版本，适用于单人使用；
- `lovers.html` 为多人版本，可用于情侣使用；
  - 还需要在 LeanCloud 后台创建一个 `Number` 类型，名为「type」的列；
  - 简单更改下文发送脚本，在 HTTP 请求体内新增 `type` 字段，并设置为 0-n 的数字，代表不同人员；
  - 目前只设置了 type 为 0 和 1 的颜色，多余的需要手动设置；

## 发送脚本

| 平台    | 支持自定义 HTTP 的应用                                       | 模板地址                                                     |
| ------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Windows | [Quicker](https://www.getquicker.net/)（可直接使用）         | [点击安装](https://getquicker.net/sharedaction?code=eeb80278-5f53-4b0d-d333-08d7e0dd26a9)<br>[最新基础版本](https://getquicker.net/sharedaction?code=6f13a847-1543-4a88-5a41-08d7fefdcaef)<br>[多人版本](https://getquicker.net/sharedaction?code=b07a57b9-dd67-40fc-5a40-08d7fefdcaef)|
| macOS   | 1. 使用 Python 脚本 + 命令行发布；<br />2. 使用 uTool 快捷命令发布； | [1. 教程与安装](https://www.skyue.com/blog/20042614.html)<br />2. [教程与安装](https://xwlearn.com/howto-graciously-bb-in-mac/) |
| iOS     | 快捷指令                                                     | [点击安装](https://www.icloud.com/shortcuts/3cfcbc36a6a24e0a8721bfeef8dfc6cf) |
| Android | [Tasker](https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm&hl=en_US) | [教程与安装](https://github.com/jimlee2002/nonsense.fun_tasker) |

- 可以查阅 LeanCloud [文档](https://console.leancloud.app/docs/rest_api.html#hash1094926014)使用任意能发送 HTTP 请求的工具发送数据；
- 可以利用 IFTTT 的 [Webhook](https://ifttt.com/maker_webhooks) ，在脚本中增加「同步到 Twitter/Facebook/Instagram 的功能」；
- 可以利用 [Telegram bot](https://core.telegram.org/bots/api) ，在脚本中增加「同步到 Channel 功能」；



# 功能

- [x]  链接解析
- [ ] RSS
- [ ] 标签
- [ ] 上传图片
- [ ] 微博搬家脚本

~~暂时不计划加入定位、上传图片等功能，因为这些功能的引入会使脚本的发送流程变得复杂，于「保卫表达、鼓励表达」的初衷无益。~~
