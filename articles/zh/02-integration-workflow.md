# 从一键调色到导出：移动端修图 SDK 的接入设计

> 一套好接入的美颜调色 SDK，不应该只给效果，也应该给产品链路、参数体系和预览导出一致性。  
> GitHub: [18818474455/ChromaBeautySDK](https://github.com/18818474455/ChromaBeautySDK)  
> 安卓 Demo APK: [chroma-beauty-android-demo-v1.0.0.apk](https://github.com/18818474455/ChromaBeautySDK/releases/download/android-demo-v1.0.0/chroma-beauty-android-demo-v1.0.0.apk)

![Chroma Demo Workflow](https://raw.githubusercontent.com/18818474455/ChromaBeautySDK/main/assets/apk-demo/demo-storyboard.jpg)

## 接入 SDK 时真正要考虑什么？

很多团队评估图像 SDK 时，第一反应是看效果图。但真正落地到 App 里，还需要关注这些问题：

- 能不能快速接进现有编辑器？
- AI 推荐结果能不能继续微调？
- 预览和最终导出会不会不一致？
- 参数是否能做埋点、保存、复用和模板化？
- 中低端机型是否可以做质量分档？
- 不同产品能否只接入需要的模块？

Chroma Beauty SDK 的设计目标，是把美颜调色能力拆成可以组合的模块，同时保留完整工作流。

## 推荐工作流

![Demo Flow](https://raw.githubusercontent.com/18818474455/ChromaBeautySDK/main/assets/apk-demo/demo-flow.gif)

一个完整的人像修图链路可以设计为：

```text
Image Input
-> AI Analyze
-> Auto Color
-> Portrait Protection
-> Beauty / Shape Controls
-> Before / After Preview
-> High Quality Export
```

在产品层面，可以对应成：

| 产品环节 | SDK 能力 |
|---|---|
| 导入图片 | 解码、尺寸管理、预览准备 |
| AI 分析 | 场景判断、人像区域、推荐参数 |
| 一键调色 | 自动生成基础光影和色彩参数 |
| 人像保护 | 控制人物区域色偏和过度增强 |
| 参数微调 | 基础、细节、颜色、风格、美颜等面板 |
| 对比预览 | 长按对比、撤销重做、效果强度 |
| 导出成片 | 复用同一参数体系，减少保存变样 |

## 参数面板如何组织？

![Color Panel](https://raw.githubusercontent.com/18818474455/ChromaBeautySDK/main/assets/apk-demo/color-panel.jpg)

建议将 UI 拆为五个面板：

| 面板 | 常见参数 |
|---|---|
| 基础 | 曝光、对比、高光、阴影、白色、黑色 |
| 细节 | 锐化、清晰度、纹理、降噪 |
| 颜色 | 色温、色调、自然饱和度、饱和度、HSL |
| 风格 | LUT、曲线、胶片、清透、人像风格 |
| 美颜 | 磨皮、美白、红润、去油光、美型、瘦身 |

这种拆法的好处是：AI 推荐可以输出完整参数，用户手动调整也能落在同一组参数里。产品后续做模板、预设、历史记录、云端配置时会更自然。

## 完整接入和模块化接入

### 完整工作台模式

适合从 0 做相机、修图、美颜工具：

```text
图片输入 -> AI 推荐 -> 调色 -> 美颜 -> 对比 -> 导出
```

这种方式适合快速做 Demo、试用版、垂直 App 或完整影像工具。

### 模块化接入模式

适合已有编辑器，只增强某个能力：

```text
只接 AI 一键调色
只接人像保护
只接美颜精修
只接美型 / 身材
只接 LUT / HSL / 手动调色
```

模块化接入对已有产品更友好，不需要推翻原有 UI 和业务流程。

## 预览与导出一致性

移动端图像产品很容易遇到一个问题：编辑时看起来不错，保存后却变了。原因可能是预览链路和导出链路不一致，或者低分辨率预览和高分辨率导出的参数没有对齐。

建议接入时把参数体系统一起来：

- 预览阶段用快速路径，保证滑杆响应；
- 导出阶段用高质量路径，保证成片稳定；
- 两者复用同一组参数，避免用户感知差异；
- 参数可序列化，方便保存草稿和复用模板。

## 商业交付建议

如果用于商业项目评估，可以准备这些信息：

| 信息 | 说明 |
|---|---|
| 目标平台 | Android / iOS / Flutter / Server Batch |
| 产品类型 | 相机、修图、社交、电商、活动摄影等 |
| 需要模块 | 调色、美颜、人像保护、美型、导出 |
| 目标机型 | 是否需要中低端机优化 |
| UI 形态 | 完整工作台或已有编辑器接入 |
| 交付方式 | SDK 包、Demo 工程、参数文档、定制调参 |

## 联系方式

GitHub: [https://github.com/18818474455/ChromaBeautySDK](https://github.com/18818474455/ChromaBeautySDK)  
Email: [yunxiangchuanlaobiao@yunxiangchuan.cn](mailto:yunxiangchuanlaobiao@yunxiangchuan.cn)

公开仓库仅用于展示，不包含正式 SDK、模型权重、私有源码或商业授权密钥。
