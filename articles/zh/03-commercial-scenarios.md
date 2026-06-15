# 面向相机、社交和电商人像的 AI 美颜调色方案

> Chroma Beauty SDK 适合把“照片变好看”变成可接入、可配置、可商业交付的产品能力。  
> 商务联系: [yunxiangchuanlaobiao@yunxiangchuan.cn](mailto:yunxiangchuanlaobiao@yunxiangchuan.cn)

![Chroma Beauty SDK](https://raw.githubusercontent.com/18818474455/ChromaBeautySDK/main/assets/apk-demo/demo-storyboard.jpg)

## 为什么行业场景需要不同处理策略？

同样是人像增强，相机、社交、电商和活动摄影的目标并不一样。

自拍相机更关心实时预览和用户体验；社交产品更关心头像和资料图的自然感；电商人像更关心肤色稳定和商品展示；活动摄影更关心批量处理效率和复杂灯光下的出片率。

Chroma Beauty SDK 可以围绕不同场景组合调色、美颜、人像保护和导出能力。

## 场景一：美颜相机 / 自拍工具

自拍产品的重点是“打开就好看”，但不能让用户觉得假。

可组合能力：

- 一键调色，让画面更明亮通透；
- 磨皮、美白、红润，让肤色更干净；
- 去油光和黑眼圈优化，提升精修感；
- 美型和五官参数，满足个性化调整；
- 长按对比，降低用户对强效果的不确定感。

![Beauty Controls](https://raw.githubusercontent.com/18818474455/ChromaBeautySDK/main/assets/apk-demo/beauty-shape-controls.jpg)

## 场景二：社交 / 婚恋 / 头像产品

社交类产品更怕“过度修图”。头像和资料图需要好看，但也要自然可信。

推荐策略：

| 模块 | 目标 |
|---|---|
| 人像保护 | 保持肤色稳定 |
| 轻量磨皮 | 提升皮肤观感，不丢真实感 |
| 色彩优化 | 让背景更干净，人物更突出 |
| 风格预设 | 给用户快速选择不同氛围 |
| 导出一致 | 避免上传后和预览差异过大 |

![Style Panel](https://raw.githubusercontent.com/18818474455/ChromaBeautySDK/main/assets/apk-demo/style-panel.jpg)

## 场景三：电商人像 / 模特图优化

电商图更强调稳定和统一。不同光线、不同场地、不同模特图，如果颜色差异太大，会影响店铺视觉一致性。

Chroma 可用于：

- 批量人像肤色统一；
- 背景和人物分层优化；
- 控制白色衣服、高光和肤色污染；
- 建立品牌风格预设；
- 做活动图、详情页图、模特图后处理。

![Color Panel](https://raw.githubusercontent.com/18818474455/ChromaBeautySDK/main/assets/apk-demo/color-panel.jpg)

## 场景四：婚礼、会议、活动照片快修

活动现场通常光线复杂：LED 屏偏色、舞台灯强、背景杂、多人合影多。传统滤镜很容易让背景更有氛围，但人物肤色变得不稳定。

更适合的链路是：

```text
照片导入
-> AI 识别画面问题
-> 增强背景氛围
-> 人像保护
-> 手动微调
-> 批量导出
```

![Demo Flow](https://raw.githubusercontent.com/18818474455/ChromaBeautySDK/main/assets/apk-demo/demo-flow.gif)

## 场景五：AIGC 图片后处理

AIGC 图片常见问题包括肤色不稳定、局部过度锐化、风格不统一、人物边缘处理不自然。Chroma 可以作为后处理链路的一部分，对生成图做统一调色、人像增强和风格修正。

这类场景不一定需要完整 UI，也可以只接入某些模块，比如：

- AI 调色；
- LUT / 风格统一；
- 皮肤区域优化；
- 导出前质量增强。

## 商业合作可以怎么谈？

建议先明确以下四个问题：

| 问题 | 示例 |
|---|---|
| 使用场景 | 相机、修图、电商、社交、活动摄影 |
| 目标平台 | Android、iOS、Flutter、服务端 |
| 需要模块 | 调色、美颜、美型、人像保护、导出 |
| 交付方式 | SDK、Demo、API 文档、定制参数、OEM |

## 联系方式

GitHub: [https://github.com/18818474455/ChromaBeautySDK](https://github.com/18818474455/ChromaBeautySDK)  
Email: [yunxiangchuanlaobiao@yunxiangchuan.cn](mailto:yunxiangchuanlaobiao@yunxiangchuan.cn)

当前公开仓库只展示产品能力和 Demo 素材，不包含正式 SDK、模型权重、APK 安装包、私有源码或授权密钥。
