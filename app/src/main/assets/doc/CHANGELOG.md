******

### 版本历史

******

# v6.1.0

###### 2022/05/26 - 包名变更 谨慎升级

* `提示` 修改应用包名为 org.autojs.autojs6 避免与开源 Auto.js 应用包名冲突
* `新增` 首页抽屉增加 "投影媒体权限" 开关 (Root / ADB 方式) (开关状态检测为实验性)
* `新增` 文件浏览器支持显示隐藏文件和文件夹 (参阅 设置页面)
* `新增` 强制 Root 检查功能 (参阅 设置页面 及 示例代码)
* `新增` 内置 autojs 模块 (参阅 示例代码 > AutoJs6)
* `新增` 内置 tasks 模块 (参阅 示例代码 > 任务)
* `新增` console.launch() 方法启动日志活动页面
* `新增` util.morseCode 工具 (参阅 示例代码 > 工具 > 摩斯电码)
* `新增` util.versionCodes 工具 (参阅 示例代码 > 工具 > 安卓版本信息查询)
* `新增` util.getClass() 等方法 (参阅 示例代码 > 工具 > 获取类与类名)
* `新增` timers.setIntervalExt() 方法 (参阅 示例代码 > 定时器 > 条件周期执行)
* `新增` colors.toInt() / rgba() 等方法 (参阅 示例代码 > 图像与颜色 > 基本颜色转换)
* `新增` automator.isServiceEnabled() / ensureService() 方法
* `新增` automator.lockScreen() 等方法 (参阅 示例代码 > 无障碍服务 > 安卓 9 新增)
* `新增` automator.headsethook() 等方法 (参阅 示例代码 > 无障碍服务 > 安卓 11 新增)
* `新增` automator.captureScreen() 方法 (参阅 示例代码 > 无障碍服务 > 获取屏幕截图)
* `新增` dialogs.build() 选项参数属性 animation, linkify 等 (参阅 示例代码 > 对话框 > 个性化对话框)
* `修复` dialogs.build() 选项参数属性 inputHint, itemsSelectedIndex 等功能异常
* `修复` JsDialog#on('multi_choice') 回调参数功能异常
* `修复` UiObject#parent().indexInParent() 总是返回 -1 的问题 _[`issue #16`](https://github.com/SuperMonster003/AutoJs6/issues/16)_
* `修复` Promise.resolve() 返回的 Thenable 在临近脚本结束时可能不被调用的问题
* `修复` 包名或类名中可能的拼写失误 (boardcast -> broadcast / auojs -> autojs)
* `修复` images.requestScreenCapture() 在高版本安卓系统可能导致应用崩溃的问题 (API >= 31)
* `修复` images.requestScreenCapture() 多个脚本实例同时申请可能导致应用崩溃的问题
* `修复` 调用 new RootAutomator() 可能出现的假死问题
* `优化` RootAutomator 在无 Root 权限时将无法实例化
* `优化` 重新设计 "关于应用与开发者" 页面
* `优化` 重构全部内置 JavaScript 模块
* `优化` 重构全部 Gradle 构建脚本并增加公共配置脚本 (config.gradle)
* `优化` Gradle 构建工具支持版本号自动管理及构建文件自动命名
* `优化` Gradle 构建工具增加 task 支持附加 CRC32 摘要到构建文件 (appendDigestToReleasedFiles)
* `优化` shell() 调用时将异常写入返回结果而非直接将异常抛出 (无需 try/catch)
* `优化` 使用 Rhino 内置的 JSON 替代原 json2 模块
* `优化` auto.waitFor() 支持超时参数
* `优化` threads.start() 支持箭头函数参数
* `优化` console.trace() 支持按日志等级参数 (参阅 示例代码 > 控制台 > 打印调用栈)
* `优化` device.vibrate() 支持模式震动及摩斯电码震动 (参阅 示例代码 > 设备 > 模式震动 / 摩斯电码震动)
* `优化` 外部存储读写权限适配高版本安卓系统 (API >= 30)
* `优化` 控制台字体采用 Material Color 增强普通及夜间主题下的字体可读性
* `优化` 保存 ImageWrapper 所有实例弱引用并在脚本结束时自动回收 (实验性)
* `优化` 附加 CircleImageView 版本 3.1.0
* `优化` 升级 Android Analytics 版本 13.1.0 -> 13.3.0
* `优化` 升级 Android Gradle 插件版本 7.3.0-alpha06 -> 7.4.0-alpha02
* `优化` 升级 Android Job 版本 1.4.2 -> 1.4.3
* `优化` 升级 Android Material 版本 1.5.0 -> 1.6.0
* `优化` 升级 CrashReport 版本 2.6.6 -> 4.0.4
* `优化` 升级 Glide 版本 4.13.1 -> 4.13.2
* `优化` 升级 Joda Time 版本 2.10.13 -> 2.10.14
* `优化` 升级 Kotlin Gradle 插件版本 1.6.10 -> 1.6.21
* `优化` 升级 Kotlinx Coroutines 版本 1.6.0 -> 1.6.1-native-mt
* `优化` 升级 Leakcanary 版本 2.8.1 -> 2.9.1
* `优化` 升级 Okhttp3 版本 5.0.0-alpha.6 -> 5.0.0-alpha.7
* `优化` 升级 Rhino 引擎版本 1.7.14 -> 1.7.15-snapshot
* `优化` 升级 Zip4j 版本 2.9.1 -> 2.10.0
* `优化` 移除 Groovy JSON 版本 3.0.8
* `优化` 移除 Kotlin Stdlib JDK7 版本 1.6.21

# v6.0.3

###### 2022/03/19

* `新增` 多语言切换功能 (尚不完善)
* `新增` 内置 recorder 模块 (参阅 示例代码 > 计时器)
* `新增` 使用 "修改安全设置权限" 自动启用无障碍服务及开关设置
* `修复` 点击 "快速设置" 中相关图标后面板未自动收起的问题 (试修) _[`issue #7`](https://github.com/SuperMonster003/AutoJs6/issues/7)_
* `修复` toast 使用强制显示参数时可能导致 AutoJs6 崩溃的问题
* `修复` Socket 传输数据头部信息不完整时可能导致 AutoJs6 崩溃的问题
* `优化` 启动或重启 AutoJs6 时根据选项设置自动开启无障碍服务
* `优化` 开启悬浮窗显示时尝试自动开启无障碍服务
* `优化` 所有资源文件补全元素对应的英文翻译
* `优化` 微调主页抽屉布局 减小项目排列间距
* `优化` 主页抽屉增加前台服务状态开关的同步
* `优化` 主页抽屉展开时立即按需同步开关状态
* `优化` 显示指针位置增加状态检测及结果提示
* `优化` 支持 64 位操作系统 (Ref to TonyJiangWJ)
* `优化` 悬浮窗初始化时同时应用透明度设置 (无需点击后再应用透明度)
* `优化` 重置文件内容时增加是否为示例代码文件的检测并增加结果提示
* `优化` 转移打包插件下载地址 GitHub -> JsDelivr
* `优化` 附加 Zeugma Solutions LocaleHelper 版本 1.5.1
* `优化` 降级 Android Material 版本 1.6.0-alpha02 -> 1.5.0
* `优化` 升级 Kotlinx Coroutines 版本 1.6.0-native-mt -> 1.6.0
* `优化` 升级 OpenCV 版本 3.4.3 -> 4.5.4 -> 4.5.5 (Ref to TonyJiangWJ)
* `优化` 升级 Okhttp3 版本 3.10.0 -> 5.0.0-alpha.4 -> 5.0.0-alpha.6
* `优化` 升级 Android Gradle 插件版本 7.2.0-beta01 -> 7.3.0-alpha06
* `优化` 升级 Auto.js-ApkBuilder 版本 1.0.1 -> 1.0.3
* `优化` 升级 Glide Compiler 版本 4.12.0 -> 4.13.1
* `优化` 升级 Gradle 发行版本 7.4-rc-2 -> 7.4.1
* `优化` 升级 Gradle Compile 版本 31 -> 32
* `优化` 升级 Gson 版本 2.8.9 -> 2.9.0

# v6.0.2

###### 2022/02/05

* `新增` images.bilateralFilter() 双边滤波图像处理方法
* `修复` 多次调用 toast 只生效最后一次调用的问题
* `修复` toast.dismiss() 可能无效的问题
* `修复` 客户端模式及服务端模式开关可能无法正常工作的问题
* `修复` 客户端模式及服务端模式开关状态不能正常刷新的问题
* `修复` Android 7 解析 UI 模式 text 元素异常 (Ref to TonyJiangWJ) _[`issue #4`](https://github.com/SuperMonster003/AutoJs6/issues/4)_ _[`#9`](https://github.com/SuperMonster003/AutoJs6/issues/9)_
* `优化` 忽略 sleep() 的 ScriptInterruptedException 异常
* `优化` 附加 Androidx AppCompat (Legacy) 版本 1.0.2
* `优化` 升级 Androidx AppCompat 版本 1.4.0 -> 1.4.1
* `优化` 升级 Androidx Preference 版本 1.1.1 -> 1.2.0
* `优化` 升级 Rhino 引擎版本 1.7.14-snapshot -> 1.7.14
* `优化` 升级 Okhttp3 版本 3.10.0 -> 5.0.0-alpha.3 -> 5.0.0-alpha.4
* `优化` 升级 Android Material 版本 1.6.0-alpha01 -> 1.6.0-alpha02
* `优化` 升级 Android Gradle 插件版本 7.2.0-alpha06 -> 7.2.0-beta01
* `优化` 升级 Gradle 发行版本 7.3.3 -> 7.4-rc-2

# v6.0.1

###### 2022/01/01

* `新增` 连接 VSCode 插件支持客户端 (LAN) 及服务端 (LAN/ADB) 方式 (Ref to Auto.js Pro)
* `新增` 内置 base64 模块 (Ref to Auto.js Pro)
* `新增` 增加 isInteger/isNullish/isPlainObject/isPrimitive/isReference 全局方法
* `新增` 增加 polyfill (Object.getOwnPropertyDescriptors)
* `新增` 增加 polyfill (Array.prototype.flat)
* `优化` 扩展 global.sleep 支持 随机范围/负数兼容
* `优化` 扩展 global.toast 支持 时长控制/强制覆盖控制/dismiss
* `优化` 包名对象全局化 (okhttp3/androidx/de)
* `优化` 升级 Android Material 版本 1.5.0-beta01 -> 1.6.0-alpha01
* `优化` 升级 Android Gradle 插件版本 7.2.0-alpha04 -> 7.2.0-alpha06
* `优化` 升级 Kotlinx Coroutines 版本 1.5.2-native-mt -> 1.6.0-native-mt
* `优化` 升级 Kotlin Gradle 插件版本 1.6.0 -> 1.6.10
* `优化` 升级 Gradle 发行版本 7.3 -> 7.3.3

# v6.0.0

###### 2021/12/01

* `新增` 主页抽屉底部增加重启应用按钮
* `新增` 主页抽屉增加忽略电池优化/显示在其他应用上层等开关
* `修复` 应用初始安装后部分区域主题颜色渲染异常的问题
* `修复` sign.property 不存在时无法 build 的问题
* `修复` 定时任务面板一次性任务的月份存取错误
* `修复` 应用设置页面开关颜色不随主题变更的问题
* `修复` 无法识别打包插件及打包插件下载地址无效的问题
* `修复` 首页抽屉 "查看使用情况权限" 开关状态可能不同步的问题
* `修复` TemplateMatching.fastTemplateMatching 潜在的 Mat 内存泄漏问题
* `优化` 升级 Rhino 引擎版本 1.7.7.2 -> 1.7.13 -> 1.7.14-snapshot
* `优化` 升级 OpenCV 版本 3.4.3 -> 4.5.4
* `优化` ViewUtil.getStatusBarHeight 提升兼容性
* `优化` 主页抽屉移除用户登录相关模块并移除布局占位
* `优化` 主页移除社区及市场标签页面并优化布局对其方式
* `优化` 修改一些设置选项的默认开关状态
* `优化` 关于页面增加 SinceDate 并优化 Copyright 显示
* `优化` 升级 JSON 模块至 2017-06-12 版本并整合 cycle.js
* `优化` 移除 Activity 前置时的自动检查更新功能并移除检查更新相关按钮
* `优化` AppOpsKt#isOpPermissionGranted 内部代码逻辑
* `优化` ResourceMonitor 使用 ReentrantLock 增强安全性 (Ref to TonyJiangWJ)
* `优化` 使用 Maven Central 等仓库替换 JCenter 仓库
* `优化` 抽离并移除重复的本地库文件
* `优化` 本地化 CrashReport 版本 2.6.6
* `优化` 本地化 MutableTheme 版本 1.0.0
* `优化` 附加 Androidx Preference 版本 1.1.1
* `优化` 附加 SwipeRefreshLayout 版本 1.1.0
* `优化` 升级 Android Analytics 版本 7.0.0 -> 13.1.0
* `优化` 升级 Android Annotations 版本 4.5.2 -> 4.8.0
* `优化` 升级 Android Gradle 插件版本 3.2.1 -> 4.1.0 -> 7.0.3 -> 7.2.0-alpha04
* `优化` 升级 Android Job 版本 1.2.6 -> 1.4.2
* `优化` 升级 Android Material 版本 1.1.0-alpha01 -> 1.5.0-beta01
* `优化` 升级 Androidx MultiDex 版本 2.0.0 -> 2.0.1
* `优化` 升级 Apache Commons Lang3 版本 3.6 -> 3.12.0
* `优化` 升级 Appcompat 版本 1.0.2 -> 1.4.0
* `优化` 升级 ButterKnife Gradle 插件版本 9.0.0-rc2 -> 10.2.1 -> 10.2.3
* `优化` 升级 ColorPicker 版本 2.1.5 -> 2.1.7
* `优化` 升级 Espresso Core 版本 3.1.1-alpha01 -> 3.5.0-alpha03
* `优化` 升级 Eventbus 版本 3.0.0 -> 3.2.0
* `优化` 升级 Glide Compiler 版本 4.8.0 -> 4.12.0 -> 4.12.0
* `优化` 升级 Gradle Build Tool 版本 29.0.2 -> 30.0.2
* `优化` 升级 Gradle Compile 版本 28 -> 30 -> 31
* `优化` 升级 Gradle 发行版本 4.10.2 -> 6.5 -> 7.0.2 -> 7.3
* `优化` 升级 Groovy-Json 插件版本 3.0.7 -> 3.0.8
* `优化` 升级 Gson 版本 2.8.2 -> 2.8.9
* `优化` 升级 JavaVersion 版本 1.8 -> 11 -> 16
* `优化` 升级 Joda Time 版本 2.9.9 -> 2.10.13
* `优化` 升级 Junit 版本 4.12 -> 4.13.2
* `优化` 升级 Kotlin Gradle 插件版本 1.3.10 -> 1.4.10 -> 1.6.0
* `优化` 升级 Kotlinx Coroutines 版本 1.0.1 -> 1.5.2-native-mt
* `优化` 升级 Leakcanary 版本 1.6.1 -> 2.7
* `优化` 升级 LicensesDialog 版本 1.8.1 -> 2.2.0
* `优化` 升级 Material Dialogs 版本 0.9.2.3 -> 0.9.6.0
* `优化` 升级 Okhttp3 版本 3.10.0 -> 5.0.0-alpha.2 -> 5.0.0-alpha.3
* `优化` 升级 Reactivex RxJava2 RxAndroid 版本 2.0.1 -> 2.1.1
* `优化` 升级 Reactivex RxJava2 版本 2.1.2 -> 2.2.21
* `优化` 升级 Retrofit2 Converter Gson 版本 2.3.0 -> 2.9.0
* `优化` 升级 Retrofit2 Retrofit 版本 2.3.0 -> 2.9.0
* `优化` 升级 Zip4j 版本 1.3.2 -> 2.9.1