---
source-updated-at: '2024-01-25T21:28:06.000Z'
translation-updated-at: '2025-05-01T17:45:17.310Z'
name: Update On Drag
route: /api/update-on-drag
menu: API
title: 拖拽时更新
---
## 示例
想直接查看实现方式？请参考以下示例：

- [update-on-drag](../../examples/react/update-on-drag)

以下 API 描述了如何使用 **update-on-drag** 功能。

## 配置项

### onDrag

```ts
onDrag: (instance: Ranger<TTrackElement>) => void
```
当拖动操作手柄 (handle) 时触发的回调函数
