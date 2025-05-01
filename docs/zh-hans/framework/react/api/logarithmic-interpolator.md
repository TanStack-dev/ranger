---
source-updated-at: '2024-01-25T21:28:06.000Z'
translation-updated-at: '2025-05-01T17:45:07.239Z'
name: Logarithmic Interpolator
route: /api/logarithmic-interpolator
menu: API
title: 对数插值器
---
## 示例
想直接查看实现方式？请参考以下示例：

- [对数插值器 (logarithmic-interpolator)](../examples/logarithmic-interpolator)

下方 API 描述了如何使用**对数插值器 (logarithmic-interpolator)** 功能。

## 配置项

默认情况下，`react-ranger` 在数据点之间使用线性插值，但允许您通过传递一个实现以下接口的对象，轻松自定义使用自己的插值函数。

### 插值器 (interpolator)

```tsx
interpolator: {
    getPercentageForValue: (val: number, min: number, max: number): number;
    getValueForClientX: (clientX: number, trackDims: object, min: number, max: number): number;
}
```
使用的插值器 (Interpolator)，默认为内置的线性比例插值器 (linear-scale interpolator)
 - `getPercentageForValue` - 接收数值及范围，返回该值从左到右所处位置的百分比 [0, 100]。
 - `getValueForClientX` - 接收 clientX（距离 ranger 左边缘的偏移量）以及尺寸和范围设置，将像素坐标转换回数值。
