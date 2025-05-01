---
source-updated-at: '2024-01-25T21:28:06.000Z'
translation-updated-at: '2025-05-01T17:45:27.115Z'
name: Custom Steps
route: /api/custom-steps
menu: API
title: 自定义步长
---
## 示例
想直接查看实现方式？请参考以下示例：

- [custom-steps](../examples/custom-steps)

以下 API 描述了如何使用 **custom-steps** 功能。

## 配置项

### steps

```ts
steps: Array<number>
```
自定义步长数组，该配置会覆盖 `stepSize`

### ticks

```ts
ticks: Array<number>
```
自定义刻度数组，该配置会覆盖 `tickSize`

## API

### getTicks
```tsx
getTicks: () => ReadonlyArray<{value: number; key: number; percentage: number}>
```
需要渲染的刻度集合。每个 `tick` 包含以下属性：
  - `value: number` - 待显示的刻度数值
  - `key: number` - 刻度的唯一键
  - `percentage: number` - 刻度在滑动条上的百分比位置
