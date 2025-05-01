---
source-updated-at: '2024-01-25T21:28:06.000Z'
translation-updated-at: '2025-05-01T17:47:34.664Z'
name: Custom Steps
route: /api/custom-steps
menu: API
title: 自訂步長
---
## 範例
想直接查看實作方式嗎？請參考以下範例：

- [custom-steps](../examples/custom-steps)

以下 API 說明將介紹如何使用 **custom-steps** 功能。

## 選項

### steps

```ts
steps: Array<number>
```
自訂步驟的陣列。此設定會覆寫 `stepSize`

### ticks

```ts
ticks: Array<number>
```
自訂刻度 (ticks) 的陣列。此設定會覆寫 `tickSize`

## API

### getTicks
```tsx
getTicks: () => ReadonlyArray<{value: number; key: number; percentage: number}>
```
需渲染的刻度 (ticks)。每個 `tick` 包含以下屬性：
  - `value: number` - 要顯示的刻度數值
  - `key: number` - 刻度的鍵值 (key)
  - `percentage: number` - 刻度在範圍選擇器 (ranger) 上的百分比位置
