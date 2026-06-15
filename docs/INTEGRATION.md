# Integration Guide

This document shows the recommended commercial integration flow for Chroma Beauty SDK. The final API shape can be adjusted for Android, iOS, Flutter, or private deployment.

## 1. Typical Flow

```text
Initialize SDK
-> Load license and model resources
-> Import image
-> Run AI analysis
-> Apply auto color / portrait protection / beauty params
-> Preview
-> Export
```

## 2. Android-style Pseudocode

```kotlin
val engine = ChromaBeautyEngine.create(
    context = context,
    license = licenseConfig,
    quality = ChromaQuality.Balanced
)

val image = engine.loadImage(uri)
val analysis = engine.analyze(image)

val autoParams = engine.recommendAutoColor(
    image = image,
    analysis = analysis,
    portraitProtect = true
)

val beautyParams = ChromaBeautyParams(
    smooth = 0.45f,
    whiten = 0.25f,
    rosy = 0.12f,
    deOil = 0.35f,
    slimFace = 0.18f,
    longLeg = 0.20f
)

val preview = engine.renderPreview(
    image = image,
    colorParams = autoParams,
    beautyParams = beautyParams
)

val output = engine.export(
    image = image,
    colorParams = autoParams,
    beautyParams = beautyParams,
    maxLongEdge = 4096
)
```

## 3. Recommended Quality Levels

| Level | Scenario | Recommendation |
|---|---|---|
| Fast | Dragging sliders, low-end devices | Lower preview resolution and lightweight model pass |
| Balanced | Normal on-screen preview | Default interactive experience |
| High | Final export | Higher resolution render and stronger quality checks |

## 4. Integration Checklist

- Confirm target platform: Android, iOS, Flutter, or custom.
- Confirm required modules: auto color, portrait protection, skin retouch, face/body reshape.
- Confirm UI mode: full editor workflow or modular integration.
- Prepare test photos: selfie, group photo, dark light, stage photo, e-commerce image.
- Define default presets and maximum effect strength.
- Add license verification and resource packaging.
- Verify preview/export consistency on real devices.

## 5. Commercial Delivery Notes

The public GitHub repository does not include model weights, SDK binaries, or private implementation details. Production delivery can be arranged separately with license control, model protection, integration support, and custom effect tuning.

