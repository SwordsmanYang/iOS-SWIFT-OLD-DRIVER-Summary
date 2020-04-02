# iOS-SWIFT-OLD-DRIVER-Summary

### About

[掘金老司机iOS周报](https://juejin.im/user/5a52075e6fb9a01c9d31b107)横向汇总（96-107期）绝大部分来源于老司机周报但不限于此，少部分文章没有引入

## 目录
- [优化@](#优化)
- [内存管理@](#内存管理)
- [跨平台@](#跨平台)
- [动画@](#动画)
- [Swift@](#Swift)
- [工具@](#工具)
- [第三方库@](#第三方库)
- [面试@](#面试)
- [原理@](#原理)
- [玩的花@](#玩的花)
- [工具@](#工具)

#### 优化@
* [为什么 Debug Information Format 改为 DWARF 可以提高编译速度？](https://mp.weixin.qq.com/s/97h0oeotOpyTc_a-9ZSJtQ) 
* [性能深度分析之System Trace](https://mp.weixin.qq.com/s/wTF3JSFH5b2zIUYAbnC-Bw) 
* [基于时间轮片方式处理超时任务](https://juejin.im/post/5e733e4f51882549417fe9aa) 
* [基于时间轮片方式处理超时任务](https://mp.weixin.qq.com/s/odkqXKHkshXKS_ZPk_EhBA) 
* [Avoiding massive SwiftUI views](https://www.swiftbysundell.com/articles/avoiding-massive-swiftui-views/) - 如何在基于 SwiftUI 开发的前提下，将 UI 分解成更小的模块，让职责更单一
* [使用 protocol 和 callAsFunction 改进 Delegate](https://onevcat.com/2020/03/improve-delegate/) 
* [ iOS Performance tips you probably didn't know](https://www.fadel.io/blog/posts/ios-performance-tips-you-probably-didnt-know/) - 文中介绍了 UILabel 和 tag 在资源占用与性能上的一些问题，并且讨论了多线程编程时的一些影响执行效率的细节
* [有赞iOS-基于二进制的编译提效策略](https://www.fadel.io/blog/posts/ios-performance-tips-you-probably-didnt-know/) - 如 Xcode 编译优化，CCache 优化等，也包含一套相对完成的 Pod 二进制方案的介绍。整体还算比较体系，比较适合不愿意投入太多时间整理架构的中小型公司参考
* [Enumerating elements in ForEach](https://oleb.net/2020/foreach-enumerated/) - 本文介绍了如何通过 SwiftUI 的 ForEach 来遍历展示列表，并对列表元素进行编号
* [ iOS中编写高效能结构体的7个要点](https://www.jianshu.com/p/1369508e477d) - 本文通过介绍在内存中一个结构体是如何被存放和使用的，来介绍在 iOS 中定义一个结构体有哪些需要注意的地方
* [ 用 struct 还是 class？让 Swift-NIO 的开发者来告诉你](https://www.dotconferences.com/2019/01/johannes-weiss-high-performance-systems-in-swift) - 稍微了解 Swift 的同学都知道 Swift Community 比较推崇使用 Struct，因为它是一种值语义，可以确保你的程序不会被各种 Side Effect 造成奇怪的影响
* [ 手淘架构组最新实践 | iOS基于静态库插桩的⼆进制重排启动优化](https://mp.weixin.qq.com/s/YDO0ALPQWujuLvuRWdX7dQ) - 本文是来自手淘架构组的谢俊逸同学在二进制重排方案的基础上，针对原有方案的一些实践限制，提出了一种基于静态库二进制插桩的重排方案，对于大量应用组件化构建应用的团队来说，是一个值得学习借鉴的好文章
* [抖音研发实践：基于二进制文件重排的解决方案 APP启动速度提升超15%](https://mp.weixin.qq.com/s?__biz=MzI1MzYzMjE0MQ==&mid=2247485101&idx=1&sn=abbbb6da1aba37a04047fc210363bcc9&scene=21#wechat_redirect) 类比上文
* [APP 网络优化之 DNS 优化实践](https://juejin.im/post/5e0d580b5188253a5c7d12fc) 网络优化中 DNS 优化又是相对重要的一块
* [iOS 微信编译速度优化分享](https://juejin.im/post/5e005f4f518825123176141a) 作者首先列举了调研过的，目前已有的编译速度优化方案，然后分享了微信使用的编译速度优化方案
* [百度 APP iOS 暗黑模式适配的完美解决方案](https://mp.weixin.qq.com/s/QOPCCIC-PbmUtuq2XUS34g) 百度研发出了一套皮肤主题框架，不仅可以全系统支持 DarkMode，还可以扩展多套皮肤主题

#### 内存管理@
* [在 ARC 下对非 ObjC 类型的指针进行操作的编译器陷阱](https://mp.weixin.qq.com/s/SE5vpD733SQw9_yc1JN_TQ) 

#### 跨平台@
* [MediaPipe - 跨平台机器学习应用开发框架](https://juejin.im/post/5e702e06e51d4526f363c62a?utm_source=gold_browser_extension) 
* [微信支付跨平台软件架构](https://mp.weixin.qq.com/s?__biz=MzAwNDY1ODY2OQ==&mid=2649287208&idx=1&sn=6f3813deaad2aa6f096bc0b0d7ba8c34&chksm=8334ceaab44347bc903bcf1d00898e124ccbc509fd628b119071b41a05959f09df2ef0716bea&mpshare=1&scene=1&srcid=&sharer_sharetime=1584703159505&sharer_shareid=c357a4972a00ef443223641b12ffbd76#rd)  
* [Weex、RN还是Flutter？资深技术专家与你聊聊阿里跨平台思路](https://mp.weixin.qq.com/s/AufpOA4ZDu0sf0sL-Sv_Sw) 
* [Flutter Platform Channel 使用与源码分析](https://juejin.im/post/5e78989cf265da575c16e75c) 
* [FlutterBoost1.0到2.0，我一共做了这几件事...](https://mp.weixin.qq.com/s?__biz=MzU4MDUxOTI5NA==&mid=2247485085&idx=1&sn=277e1c7d555099f1cb1018614810f14e&chksm=fd54d28cca235b9a16518428b7f7df249e6da193e6fa9b567f19bcf9d88790e02b888c0c93bc&token=1853870359&lang=zh_CN#rd) - 闲鱼技术
* [FLUI](https://www.flui.xin/) - 是一个基于 Flutter 开发的 UI 框架，拥有完善的使用示例和文档，同时支持动态化渲染、Dark Mode 等特性
* [打破重重阻碍，Flutter 和 Web 生态如何对接？](https://mp.weixin.qq.com/s/eL02zPLFbTOXm1vS6UEA4g)
* [Flutter 在字节跳动的现状与工程实践](https://mp.weixin.qq.com/s?__biz=MzUxMzcxMzE5Ng==&mid=2247493836&idx=1&sn=979792491d0abe803c0f00ed412fb0de&chksm=f9525d8fce25d499f5c9815529f7fc25d5e130986a44e430352e375b77d5fe727a8d88f783e1&mpshare=1&scene=1&srcid=&sharer_sharetime=1582811190556&sharer_shareid=b37c346ca5a345410d47741175cc1271&rd2werd=1#wechat_redirect) - 要分享 Flutter 在字节跳动的现状以及工程实践经验的深度好文
* [向现有应用添加 Flutter](https://mp.weixin.qq.com/s/DckZviEm6P1cNC1oZBvXKw) 

#### 动画@
* [用UIKit和UIView在视图上执行iOS动画](https://juejin.im/post/5e784681f265da57671be823) - 60 Fps动画，UIKIT/UIVIEW动画 UIViewProperty动画

#### Swift@
* [Swift 5.2 正式发布 & 5.3 正在路上](https://swift.org/blog/5-3-release-process/) 
* [手淘 App 如何落地 Swift ？一边探索实践，一边“打怪升级”](https://mp.weixin.qq.com/s/_iweRWQCjnoASCmUAKHDFA) 
* [UIAlertController with Function Builders](https://felginep.github.io/2020-03-10/uialertcontroller-function-builders) - Function Builder 是 Swift 5.1 的新特性，在 Swift 的基础上构建自己的 DSL 的语法。文章基于 Function Builder，创建简单且易读的 UIAlertController API
* [ntroducing Swift Crypto](https://swift.org/blog/crypto/)  Swift 开发人员都可以访问这些 API，以实现一系列通用的加密操作
* [The Nested Closure Trap](https://medium.com/flawless-app-stories/the-nested-closure-trap-356a0145b6d)  从 Swift 嵌套的闭包入手，提及了在多层嵌套中可能出现的内存泄漏场景
* [设计模式（Swift 5.0 实现）](https://github.com/Binlogo/Design-Patterns-In-Swift-CN)  - 全面的 Swift 5.0 示例实现的设计模式
* [ How Swift imports C APIs](https://github.com/apple/swift/blob/master/docs/HowSwiftImportsCAPIs.md)  - 当 Swift 从基于 C 的语言（C，Objective-C）导入一个模块或者解析 bridging header 时，这些语言的接口被映射为 Swift 接口以便可以在 Swift 代码中直接使用
* [  从探索到落地，手淘引入 Swift “历险记”](https://mp.weixin.qq.com/s/oHGkoGzhMs-l8TX6t0831w)  - 本文还原了手淘 iOS APP 历时一年将 Swift 语言从调研到基础设施建设，再到顺利落地业务的全过程，其推进的策略、所遇到的问题及其解决方案

#### 工具@
* [滴滴正式发布开源客户端研发助手DoKit 3.0，新特性解读](https://mp.weixin.qq.com/s/cTze8_-0KBIHHh96aEcilg)  - DoKit3.0 - 不只是工具
* [SourceKitForSafari](https://github.com/kishikawakatsumi/SourceKitForSafari)  - 提升在 github 上浏览代码的体验
* [Determining which frameworks use UIWebView](https://blog.kulman.sk/determining-which-frameworks-use-uiwebview/)  - 检测三方库是否包含 UIWebView
* [Profiling and debugging your Combine code with Timelane](https://www.donnywals.com/profiling-and-debugging-your-combine-code-with-timelane/)  -是一个响应式编程调试工具，结合 Instrument 提供更直观、交互式的调试过程，同时支持 Combine 和 RxSwift。
* [Flight rules for Git](https://github.com/k88hudson/git-flight-rules/blob/master/README_zh-CN.md)  挺不错的一个 iOS 资讯 App，而且仅看 Feed 简介的话不用翻墙哦（l可以看英文版的老司机周报）
* [CocoaHub](https://cocoahub.app/?utm_campaign=iOS%2BDev%2BWeekly&utm_medium=email&utm_source=iOS%2BDev%2BWeekly%2BIssue%2B445)  这是一篇 Git 急救指南
* [MultipeerKit](https://github.com/insidegui/MultipeerKit)  - MultipeerKit 是一个 Swift 软件包，它允许 iOS、macOS 和 tvOS 设备通过 Wi-Fi 网络，点对点 Wi-Fi 和蓝牙在它们之间交换数据
* [Xcode Build Settings](https://xcodebuildsettings.com/)  - Build Settings 有数百种配置，这个网站整理了每一个配置的含义，可以随时用来查询。结合 Mattt 的 Xcode Build Configuration Files，了解使用 xcconfig 来管理 APP 的 Build Settings
* [zld](https://juejin.im/post/5e5cc0b66fb9a07cb96af303)  - 在大型项目里增量编译 link 阶段的耗时占用非常大，Benchmark 显示 link 时间比原本缩短了 40% 左右
* [Swift 编写的 iOS 端抓包工具（Knot)](https://juejin.im/post/5e426f1a518825496f38149a)  
* [为 iOS 审核操碎了心！用岩鼠提升 iOS 审核通过率吧](https://juejin.im/post/5e1c04626fb9a03013306396)  

#### 第三方库@
* [SwiftCurrency: Type-safety and algorithms for working with money in Swift.](https://github.com/peek-travel/swift-currency)  Swift Currency 是一个在 Swift 中来表达 ISO 4217 的一个货币的库。这个库是一个类型安全的，并支持文字表达，文字插入和数学表达式等对货币的操作
* [Time: Building a better date/time library for Swift](https://github.com/davedelong/time)  Time 是一个纯 Swift 实现的日期 API 集合，提供了 SwiftPM 的方式接入。提供了一种“讲人话”的方式来操作日期和时间，比如可以简单的针对不同的时区生成 clock 对象，并能够轻而易举的从 clock 对象中拿到年月日，时分秒等信息
* [DarkModeKit](https://github.com/microsoft/FluentDarkModeKit) - Microsoft Office套件dark开源，代码质量非常高
* [KeyboardGuide](https://github.com/niw/KeyboardGuide) - 优雅的处理键盘，并且对 iPad 也提供了良好的支持

#### 面试@
* [在阿里我是如何当面试官的（持续更新）](https://juejin.im/post/5e6ebfa86fb9a07ca714d0ec)  - 不是面试iOS的，但是有很多可以学习的地方

#### 原理@
* [深入剖析 WebKit](https://ming1016.github.io/2017/10/11/deeply-analyse-webkit/#more) - 戴铭 老师关于 WebKit 的一篇文章（点进去是星光舍，这里有很多好文）
* [开源 | Objective-C & Swift 最轻量级 Hook 方案](https://mp.weixin.qq.com/s/wxigL1Clem1dR8Nkt8LLMw) -  字节跳动技术团队公众号，字节跳动技术团队带来一套基于消息转发机制的 instance 粒度的轻量级 hook 方案：SDMagicHook
* [@](https://nshipster.com/at-compiler-directives/) - Mattt 大神新作，以新手入门的视角列举并介绍了 Objective-C 中 @ 符号开头的一系列指令）[中文翻译链接](https://nshipster.cn/at-compiler-directives/) 
* [从客户端角度窥探小程序架构](https://juejin.im/post/5e0dfb8cf265da5d2076ef69) - 本文比较完整的分析了小程序的发展历程，以及简单剖析了小程序的实现方式。探讨了小程序基于 H5 的技术栈是如何实现展现与逻辑的解耦，也 cover 了小程序相关领域的常用技术方案，比如离线包和预加载等。最后简单介绍了支付宝小程序的架构。整篇文章内容相对全面，适合入门的同学阅读
* [为什么 TCP 协议有性能问题 · Why's THE Design?](https://draveness.me/whys-the-design-tcp-performance/) - 本文会分析 TCP 协议为什么在弱网环境下有严重的性能问题
* [聊聊 Symbol](https://github.com/LeoMobileDeveloper/Blogs/blob/master/Compiler/unstanding-symbol.md) - Symbol 在编译期和运行时都扮演了重要的角色，但了解 Symbol 、Symbol Table 等概念对我们在一些问题的定位甚至做程序架构都很有帮助

#### 玩的花@
* [ iPhone可以运行Android了](https://mp.weixin.qq.com/s/hYjmPNxlX8P_BiEo4LveJQ) - Project Sandcastle（沙堡计划，项目地址：projectsandcastle.org/），目前支持在 iPhone7 / 7 Plus 设备上运行 Android
* [ Barber](https://github.com/michaeleisel/barber) - @老驴：此 framework 用了点投机取巧的方式来加快项目开发中增量编译的速度问题，基本思路是去掉 AppDelegate，转而为每一个大 ViewController 各自建立自己的 dependency，这样在针对某个 ViewController 做开发的时候，可以避免小改动就导致全部重新编译的情况。
其实个人并不是很推荐在正儿八经的项目中使用这样的 framework，不过，这样的思路倒是可以参考一下
* [ 推荐一款 Postman 的开源替代品： Postwoman](https://mp.weixin.qq.com/s/8viBJ46-5-POvMftNfY-Eg) - Postwoman 是一个 Postman 的免费、快速且美观的替代方案，作为一款开源的 Postman 替代品

#### 设计模式@
* [深入分析MVC、MVP、MVVM、VIPER](https://www.jianshu.com/p/2ad25e2769b5) - 本文介绍了如何在 iOS 中使用 MVVM 架构，MVVM 各个部分如何在 iOS 中发挥作用，以及如何保持一个清晰的文件结构

#### 调试@
* [iOS 开发调试概览](https://www.cnblogs.com/kenshincui/p/11953536.html) - 简述 iOS 开发过程中，常用的一些调试手段。
