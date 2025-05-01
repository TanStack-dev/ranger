---
source-updated-at: '2024-01-25T21:28:06.000Z'
translation-updated-at: '2025-05-01T17:46:29.471Z'
name: Basic
route: /api/basic
menu: API
title: 基本
---
## 範例
想要直接查看實作方式嗎？請參考以下範例：

- [基本範例](../../examples/react/basic)

下方 API 說明將介紹如何使用**基本**功能。

## 選項

### values

```tsx
values: ReadonlyArray<number>
```
**必填** 範圍的當前數值（或多個數值）。

### min

```tsx
min: number
```
**必填** 範圍的最小限制。

### max

```tsx
max: number
```
**必填** 範圍的最大限制。

### stepSize

```ts
stepSize: number
```
**必填** 可選步驟之間的距離。

### onChange

```ts
onChange: (instance: Ranger<TTrackElement>) => void
```
當拖曳手柄釋放時會呼叫此函式。

## API

### handles
```tsx
handles: ReadonlyArray<{value: number; isActive: boolean; onKeyDownHandler(event): function; onMouseDownHandler(event): function; onTouchStart(event): function}>
```
需要渲染的手柄。每個 `handle` 具有以下屬性：
 - `value: number` - 手柄的當前數值。
 - `isActive: boolean` - 表示手柄是否正在被拖曳。
 - `onKeyDownHandler(event): func`
 - `onMouseDownHandler(event): func`
 - `onTouchStart(event): func`

### activeHandleIndex
```tsx
activeHandleIndex: null | number
```
當前被拖曳手柄的零基索引，若無手柄被拖曳則為 `null`。
