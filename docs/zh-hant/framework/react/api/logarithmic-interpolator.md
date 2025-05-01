---
source-updated-at: '2024-01-25T21:28:06.000Z'
translation-updated-at: '2025-05-01T17:46:45.336Z'
name: Logarithmic Interpolator
route: /api/logarithmic-interpolator
menu: API
title: 對數插值器
---
## 範例
想要直接查看實作方式嗎？請參考以下範例：

- [logarithmic-interpolator](../examples/logarithmic-interpolator)

以下 API 說明如何使用 **logarithmic-interpolator** 功能。

## 選項

預設情況下，`react-ranger` 會在資料點之間使用線性插值，但您可以透過傳入實作以下介面的物件，輕鬆自訂為使用自己的插值函式。

### interpolator

```tsx
interpolator: {
    getPercentageForValue: (val: number, min: number, max: number): number;
    getValueForClientX: (clientX: number, trackDims: object, min: number, max: number): number;
}
```
要使用的插值器 (Interpolator)。預設為內建的線性比例插值器 (linear-scale interpolator)
 - `getPercentageForValue` - 接收數值與範圍，並回傳該數值從左到右所處位置的百分比 [0, 100]。
 - `getValueForClientX` - 接收 clientX (與 ranger 左邊緣的偏移量) 以及尺寸和範圍設定，並將像素座標轉換回數值。
