# QQ 版本列表实用工具 for Android

![QQ 版本列表实用工具 Banner](/QQVerToolBanner.png)

<div align="center">

[注意事项](#注意事项) | [简介](#简介) | [如何使用](#如何使用) | [获取更新](#获取更新) | [常见问题](#常见问题) | [其它](#其它)

[贡献成员](#贡献成员) | [开源相关](#开源相关) | [孪生项目](#孪生项目)

</div> 

<details>

<summary>关于近期多家国内 Android OEM 系统报毒 QQ 版本列表实用工具的声明</summary>

## 关于近期多家国内 Android OEM 系统报毒 QQ 版本列表实用工具的声明

近期我们发现多家国内 Android OEM 系统（包括但不限于小米 MIUI/HyperOS、荣耀 MagicOS 等）将 QQ 版本列表实用工具列为病毒，特在此发表声明：

### 1. 产品声明与保证

QQ 版本列表实用工具严格遵守中华人民共和国相关法律法规。我们确认，该应用程序的所有代码及其更新版本均未包含任何恶意代码或病毒性质的内容。

### 2. 开源许可证声明

QQ 版本列表实用工具的源代码依据经过开源促进会（[Open Source Initiative](https://opensource.org)）认证的 GNU Affero General Public License Version 3（AGPL v3）协议开放源代码，用户可以依照协议条款自由查看、审计和使用源代码。

### 3. 法律责任

若任何个人或组织因上述误报行为遭受损害，QQ 版本列表实用工具保留依法追究法律责任的权利。

特此声明！

附 VirusTotal 对 QQ 版本列表实用工具 v1.2.2-3b425fc 的扫描结果：https://www.virustotal.com/gui/file/865f30709812664937192d55c64568f7c8df3406f0dda3faf5534e64eef756c2

</details>

<span id="注意事项"></span>

## 注意事项：使用前须知

> [!WARNING]
> 请确保您在使用前充分审慎阅读了[用户协议](/UserAgreement.md)。鉴于 QQ 测试版可能存在不可预知的稳定性问题，您在下载及使用该测试版本之前，必须明确并确保自身具备足够的风险识别和承受能力。根据相关条款，您使用本软件时应当已了解并同意，因下载或使用 QQ 测试版而可能产生的任何直接或间接损失、损害以及其他不利后果，均由您自行承担全部责任。

> [!WARNING]
> QQ 版本列表实用工具提供的所有服务及内容均旨在促进合法的学习交流活动，严禁用户将其用于任何非法、违规或侵犯他人权益的目的。敬请所有用户严格遵守相关法律法规，在使用本应用的过程中秉持合法、正当与诚信原则，切勿涉足任何违法用途。如有违反，相关法律责任将由行为人自负，同时，本应用亦保留采取一切必要措施的权利，包括但不限于暂停或终止服务，并追究其法律责任。

## 简介

QQ 版本列表实用工具 for Android 是一个使用 Material 3 组件库构建，旨在提供 Android QQ 版本列表的查看和对 Android QQ 下载链接的枚举法猜测的 Android 软件。QQ 版本列表实用工具用户可以通过本应用及时获取到 Android QQ 版本更新的最新信息。

<span id="如何使用"></span>

## 如何使用？

### 版本列表

在进入 QQ 版本列表实用工具时，您首先会看到一系列显示“x.y.z””xxx MB”的卡片，这些卡片组成的列表即为 Android QQ 的版本列表，卡片列表展示了已经或即将发布的 Android QQ 版本。版本信息来源：https://im.qq.com/rainbow/androidQQVersionList

通过点击卡片右侧箭头按钮，可展开卡片以查阅到更为详尽的信息。

默认情况下，长按卡片文字会弹出展示卡片原始 JSON 字符串的对话框，长按对话框文字可选择复制字符串内容。可在设置中关闭此功能。

### 猜版 Extended

在 Android QQ - 首页侧滑菜单 - 设置 - 关于QQ与帮助 中可得知，Android QQ 的版本号通常为 `x.y.z.nnnnn`。其中 `x.y.z` 在这里被称为“主版本号”，而 `nnnnn` 被称为“小版本号”。

在 QQ 版本列表实用工具界面，点击右下角放大镜图标浮动按钮即可进入“猜版 Extended”对话框。

对话框含有三个输入框，分别是“主版本号”、“猜版类型”和“小版本号”。“主版本号”已经预填入了版本列表显示的最新版本号，也可自行修改。

- 若选择猜正式版，无需填写小版本号，软件将尝试访问以下链接：
  - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>_64.apk`
  - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>_64_HB.apk`
  - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>_64_HB1.apk`
  - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>_64_HB2.apk`
  - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>_64_HB3.apk`
  - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>_64_BBPJ.apk`
  - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>_HB_64.apk`
  - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>_HB1_64.apk`
  - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>_HB2_64.apk`
  - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>_HB3_64.apk`
  - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>_BBPJ_64.apk`

- 若选择猜测试版，则需要填写起始小版本号：

  - 默认情况下，软件将尝试访问 `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>.<小版本号>_64.apk` ，若当次访问未果，默认情况下将按照设置逻辑自动递增小版本号后再次尝试访问，直到访问成功为止。

  - 在设置中打开扩展测试版猜版格式后，软件将尝试访问以下链接：
    <details>
    <summary>点击展开</summary>
    - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>.<小版本号>_64.apk`
    - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>.<小版本号>_64_HB.apk`
    - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>.<小版本号>_64_HB1.apk`
    - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>.<小版本号>_64_HB2.apk`
    - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>.<小版本号>_64_HB3.apk`
    - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>.<小版本号>_HB_64.apk`
    - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>.<小版本号>_HB1_64.apk`
    - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>.<小版本号>_HB2_64.apk`
    - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>.<小版本号>_HB3_64.apk`
    - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>.<小版本号>_64_HD.apk`
    - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>.<小版本号>_64_HD1.apk`
    - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>.<小版本号>_64_HD2.apk`
    - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>.<小版本号>_64_HD3.apk`
    - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>.<小版本号>_HD_64.apk`
    - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>.<小版本号>_HD1_64.apk`
    - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>.<小版本号>_HD2_64.apk`
    - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>.<小版本号>_HD3_64.apk`
    - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>.<小版本号>_64_HD1HB.apk`
    - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>.<小版本号>_HD1HB_64.apk`
    </details>

    若当次访问未果，默认情况下将按照设置逻辑自动递增小版本号后再次尝试访问，直到访问成功为止。
  
  - 设置自定义猜版后缀后，可以猜测以下直链格式：
  
    - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号><自定义后缀>.apk`
    - `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android_<主版本号>.<小版本号><自定义后缀>.apk`

> [!TIP]
> QQ 版本列表实用工具实验性支持了 Android 微信的猜版。若选择微信猜版，对话框将变更为四个输入框，分别是“主版本号”、“猜版类型”、“真实版本号”和“十六进制代码”，对应的直链为：
>
> `http://dldir1.qq.com/weixin/android/weixin<主版本号>android<真实版本号>_<十六进制代码>_arm64.apk`
>
> 填入相应输入框内容后，软件将尝试访问上述链接。若当次访问未果，默认情况下将自动递增十六进制代码后再次尝试访问，直到访问成功为止。

访问成功后，软件会弹出成功对话框，对话框下方提供了一系列动作按钮，依次是“分享”、“下载”、“停止”、“跳过”和“复制”。

> [!WARNING]
> 微信猜版功能为 QQ 版本列表实用工具附带的实验性功能，可能存在不可预知的稳定性问题。请明确并确保自身具备足够的风险识别和承受能力。

<span id="获取更新"></span>

## 获取更新

<a href='https://github.com/klxiaoniu/QQVersionList/releases'><img src='https://raw.githubusercontent.com/klxiaoniu/QQVersionList/master/ReadmeAssets/GitHub-Badge.png' width="300" alt="Get it on GitHub"></a>

<a href='/ReadmeAssets/Get-it-on-Obtainium.md'><img src='https://raw.githubusercontent.com/ImranR98/Obtainium/main/assets/graphics/badge_obtainium.png' width="300" alt="Obtanium"></a>

<a href='/ReadmeAssets/Get-it-on-JiuQi-NotifCenter-WeChatMiniProgram.md'><img src='https://raw.githubusercontent.com/klxiaoniu/QQVersionList/master/ReadmeAssets/JiuQi-NotifCenter-Badge-Dark-zh-Hans.png' width="300" alt="Get it on Notif Center"></a>

## 常见问题

### QQ 版本列表实用工具能否实现“检测到新测试版本自动提醒您”的功能？

QQ 版本列表实用工具不能实现“检测到新版本自动提醒您”的功能，因为这需要自有服务器，并且需要自有服务器去长时间请求腾讯服务器，存在法律和技术风险。

### “猜版”里的“空格猜版”是什么？

2023 年 12 月 22 日，腾讯 QQ 官方团队在上传 Android QQ 9.0.8.14600 版本时，不慎将常规链接格式 `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android.9.0.8.14600.64.apk` 错误配置为包含 URL 编码空格形式的链接地址 `https://downv6.qq.com/qqweb/QQ_1/android_apk/Android%209.0.8.14600%2064.apk`。鉴于这一异常现象，QQ 版本列表实用工具增设了“空格版”猜版模式，该功能在原有的“测试版”猜版模式上将版本号中的 `.` 字符替换为 URL 编码的空格符 `%20`，以适应并支持此类非标准但实际存在的直接下载链接。

### 为什么默认添加了小版本号必须为 5 的倍数这项限制？

基于对 Android QQ 长期以来的版本号发布规律进行深入观察和分析的结果，我们发现 Android QQ 小版本号更新通常遵循每增加一个有效版本即递增 5 的倍数这一特定模式。为了贴近这一潜在实际规范并确保 QQ 版本列表实用工具的快捷性，QQ 版本列表实用工具依据最佳实践原则，默认设置小版本号和猜版必须为 5 的倍数的限制规则。然而，对于用户而言，此项约束并非强制性，如有需要，用户可随时进入设置解除此限制选项，以便更加灵活地匹配各类版本信息。

### 版本列表中已经有新的版本号了，为什么我使用猜版却获取不到下载链接？

即使版本列表已出现了新的版本号，也并不意味着 QQ 团队已经完成了新版本（含测试版）安装包在腾讯公网服务器的部署和发布。一种可能的情况是，QQ 团队正在进行新版本的内部测试阶段，因而尚未对外提供公网下载渠道。

### 为什么不提供 Android 微信的版本列表？

目前还没有找到来自官方的可靠且请求次数少而信息密度大的 Android 微信版本列表数据源，因此 QQ 版本列表实用工具无法提供 Android 微信的版本列表。如果您发现了可靠的 Android 微信版本列表数据源，欢迎提出 Issue(s) 或提交 PR。

## 其它

> [!IMPORTANT]
> QQ 版本列表实用工具始终坚守法律底线，秉持尊重与保护所有用户及第三方合法权益的原则。我们深切认识到任何可能存在的权益侵犯行为都会对权益方造成潜在影响，对此，我们表示由衷歉意，并承诺，一旦接到权益方的权益受到侵犯的通知，我们将立即依法启动核查程序，并在确认侵权事实后，迅速采取有效措施，以最大程度地消除不良影响，恢复并保障权益方的合法权益。敬请相关权益方在发现 QQ 版本列表实用工具存在任何侵权内容时，及时与我们取得联系，我们将竭诚为权益方提供必要的协助与支持。

> [!NOTE]
> “QQ”“腾讯 QQ”“腾讯”“微信”“WeChat”是深圳市腾讯计算机系统有限公司和/或其关联公司的商标。本应用对“QQ”“腾讯 QQ”“腾讯”“微信”“WeChat”的使用旨在注明和指向对应主体，并非表示对“QQ”、“腾讯 QQ”、“腾讯”、“微信”、“WeChat”商标的注册和拥有。

> [!NOTE]
> Android™ 是 Google LLC 的商标。

## 贡献成员

<a href="https://github.com/klxiaoniu/QQVersionList/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=klxiaoniu/QQVersionList"  alt="贡献成员"/>
</a>

## 开源相关

QQ 版本列表实用工具采用 [GNU Affero General Public License Version 3](/LICENSE) 开源许可。

QQ 版本列表实用工具的诞生离不开以下开源项目，感谢以下开源项目的作者和贡献者：

- [Material Components for Android](https://github.com/material-components/material-components-android/)，Licensed under [Apache License Version 2.0](https://github.com/material-components/material-components-android/blob/master/LICENSE)
- [Android Jetpack](https://github.com/androidx/androidx/)，Licensed under [Apache License Version 2.0](https://github.com/androidx/androidx/blob/androidx-main/LICENSE.txt)
- [Remix Icon（Remix Design）](https://remixicon.com/)，Licensed under [Apache License Version 2.0](https://remixicon.com/license)
- [OkHttp（Square）](https://square.github.io/okhttp/)，Licensed under [Apache License Version 2.0](https://github.com/square/okhttp/blob/master/LICENSE.txt)
- [Kotlin（JetBrains）](https://kotlinlang.org/)，Licensed under [Apache License Version 2.0](https://github.com/JetBrains/kotlin/blob/master/license%2FREADME.md)
- [Gson（Google）](https://github.com/google/gson/)，Licensed under [Apache License Version 2.0](https://github.com/google/gson/blob/master/LICENSE)
- [Coil](https://coil-kt.github.io/coil/)，Licensed under [Apache License Version 2.0](https://github.com/coil-kt/coil/blob/main/LICENSE.txt)
- [Eclipse Temurin™](https://adoptium.net/zh-CN/temurin/)，Licensed under GNU General Public License, version 2 with the Classpath Exception
- [Oracle JDK](https://www.oracle.com/java/technologies/downloads/)，Licensed under [Oracle No-Fee Terms and Conditions](https://www.java.com/freeuselicense)
- [JetBrains Runtime](https://github.com/JetBrains/JetBrainsRuntime)，Licensed under [GNU General Public License, version 2](https://github.com/JetBrains/JetBrainsRuntime/blob/main/LICENSE)
- [Kotlin Serialization](https://github.com/Kotlin/kotlinx.serialization)，Licensed under [Apache License Version 2.0](https://github.com/Kotlin/kotlinx.serialization/blob/master/LICENSE.txt)
- [Get QQ Update Link（owo233）](https://github.com/callng/GQUL)，Licensed under [The Unlicense](https://github.com/callng/GQUL/blob/master/LICENSE)

## 孪生项目

[QQ 版本列表 Lite for WeChat MiniProgram](https://github.com/ArcticFoxPro/QQVersionListTool-WeChatMiniProgram)，Licensed under [木兰公共许可证, 第2版](https://github.com/ArcticFoxPro/QQVersionListTool-WeChatMiniProgram/blob/main/LICENSE)

[![QQ 版本列表 Lite Banner](https://raw.githubusercontent.com/ArcticFoxPro/QQVersionListTool-WeChatMiniProgram/main/QQVerLiteBanner.png)](https://github.com/ArcticFoxPro/QQVersionListTool-WeChatMiniProgram)
