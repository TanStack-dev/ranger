---
source-updated-at: '2024-01-25T21:28:06.000Z'
translation-updated-at: '2025-05-01T17:47:50.631Z'
name: Custom Styles
route: /api/custom-styles
menu: API
title: 自訂樣式
---
## 範例
想直接查看實作方式嗎？請參考以下範例：

- [custom-styles](../examples/custom-styles)

以下 API 說明如何使用的 **custom-steps** 功能。

## API

### getSegments
```tsx
getSegments: () => ReadonlyArray<{left: number; width: number}>
```
需要渲染的區段 (segments)。每個 `segment` 具有以下屬性：
  - `left: number` - 區段在範圍選擇器 (ranger) 上的起始位置百分比值
  - `width: number` - 區段寬度的百分比值
