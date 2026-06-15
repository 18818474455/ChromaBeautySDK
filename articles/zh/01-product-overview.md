# 不只是美颜滤镜：Chroma Beauty SDK 的移动端影像处理链路

> 面向相机、修图、社交、电商人像和活动摄影产品的 AI 美颜调色 SDK。  
> GitHub: [18818474455/ChromaBeautySDK](https://github.com/18818474455/ChromaBeautySDK)  
> 商务联系: [yunxiangchuanlaobiao@yunxiangchuan.cn](mailto:yunxiangchuanlaobiao@yunxiangchuan.cn)

![Chroma Beauty SDK Demo App](https://raw.githubusercontent.com/18818474455/ChromaBeautySDK/main/assets/apk-demo/demo-storyboard.jpg)

## 为什么不是再做一套滤镜？

很多图片产品表面上缺的是滤镜，实际上缺的是一条稳定的人像影像处理链路。

真实用户上传的照片往往并不理想：室内灯光混杂、舞台屏幕偏色、多人合影肤色不统一、背景氛围不够、人像一调色就发红或发灰。只靠固定滤镜，很容易出现“背景好看了，人却不自然”的问题。

Chroma Beauty SDK 的定位不是简单叠加滤镜，而是把 **AI 一键调色、人像保护、美颜精修、美型控制、预览导出** 组合成一个可落地的移动端处理方案。

## Demo App 里能看到什么？

![Demo Flow](https://raw.githubusercontent.com/18818474455/ChromaBeautySDK/main/assets/apk-demo/demo-flow.gif)

Demo 的核心路径很直接：

```text
导入图片
-> AI 推荐调色
-> 开启人像保护
-> 调整基础、细节、颜色、风格、美颜参数
-> 对比原图
-> 导出成片
```

这条路径更接近真实 App 的用户体验：普通用户可以一键得到结果，进阶用户也能继续通过参数微调。

## 一键调色：先给结果，再保留控制权

![AI One-Tap Color](https://raw.githubusercontent.com/18818474455/ChromaBeautySDK/main/assets/apk-demo/one-tap-color.jpg)

一键调色的价值，不只是把照片变亮或增加饱和度，而是根据画面内容生成一组可继续调节的参数。

Chroma 可围绕以下方向提供能力：

| 方向 | 说明 |
|---|---|
| 基础光影 | 曝光、对比、高光、阴影、白色、黑色 |
| 色彩氛围 | 色温、色调、自然饱和度、饱和度 |
| 分区调色 | HSL / Color Mixer / 主色增强 |
| 风格化 | LUT、曲线、胶片感、清透风格 |
| 安全控制 | 肤色保护、亮部保护、白衣保护、人像保护 |

对产品来说，这意味着 AI 推荐、手动滑杆、预设风格可以共享同一套处理链路，后续做版本迭代和参数定制也更清晰。

## 人像保护：背景有氛围，人脸不跑偏

很多调色方案对风景图有效，但到了人像场景就容易翻车。常见问题包括肤色发黄、脸部过曝、多人合影肤色不一致、强色背景污染人物区域。

Chroma 的人像保护思路是：背景可以增强氛围，但人物区域需要尽量保持自然。它适合活动照、商场路演、婚礼现场、舞台照片、电商人像、头像和社交资料图等场景。

## 美颜精修：不是整图模糊

![Beauty Controls](https://raw.githubusercontent.com/18818474455/ChromaBeautySDK/main/assets/apk-demo/beauty-shape-controls.jpg)

商业美颜不能只做全图模糊。用户需要皮肤更干净，但也希望眼睛、头发、衣服、背景和五官边缘保持清楚。

可组合的模块包括：

| 模块 | 产品价值 |
|---|---|
| 磨皮 | 皮肤区域更干净，尽量保留细节观感 |
| 美白 | 提升肤色明度，避免假白 |
| 红润 | 增强气色，避免过度饱和 |
| 去油光 | 控制额头、鼻梁、脸颊局部高光 |
| 黑眼圈 | 优化眼下区域观感 |
| 美型 | 脸型、眼睛、鼻子、嘴巴等五官参数 |
| 身材 | 瘦身、长腿、比例优化等产品能力 |

## 适合哪些团队？

- 美颜相机 / 自拍相机
- 图片编辑 / 滤镜修图 App
- 社交、婚恋、头像类产品
- 电商人像和模特图优化
- 婚礼、活动、会议照片快修
- AIGC 图片后处理和人像增强
- 私有化图片生产系统

## 公开仓库说明

当前 GitHub 仓库用于产品展示和技术沟通，不包含正式 SDK 二进制、模型权重、训练数据、私有源码、商业授权密钥或客户定制资料。

如需 SDK 试用、商务合作、商业授权、OEM 定制或效果调参，可以联系：

[yunxiangchuanlaobiao@yunxiangchuan.cn](mailto:yunxiangchuanlaobiao@yunxiangchuan.cn)
