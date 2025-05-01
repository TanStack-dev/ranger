---
source-updated-at: '2024-01-25T21:28:06.000Z'
translation-updated-at: '2025-05-01T17:45:33.666Z'
name: Custom Styles
route: /api/custom-styles
menu: API
title: 自定义样式
---
## 示例
想直接查看实现方式？请参考以下示例：

- [自定义样式 (custom-styles)](../examples/custom-styles)

下方 API 描述了如何使用 **自定义步骤 (custom-steps)** 功能。

## API

### getSegments
```tsx
getSegments: () => ReadonlyArray<{left: number; width: number}>
```
待渲染的分段数据。每个 `segment` 包含以下属性：
  - `left: number` - 分段在滑块 (ranger) 上的起始位置百分比值
  - `width: number` - 分段宽度的百分比值
