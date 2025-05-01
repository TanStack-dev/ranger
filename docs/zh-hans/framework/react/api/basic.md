---
source-updated-at: '2024-01-25T21:28:06.000Z'
translation-updated-at: '2025-05-01T17:45:49.199Z'
name: Basic
route: /api/basic
menu: API
title: 基础用法
---
## 示例
想要直接查看实现代码？请参考以下示例：

- [基础用法](../../examples/react/basic)

以下 API 描述了如何使用**基础**功能。

## 配置项

### values

```tsx
values: ReadonlyArray<number>
```
**必填** 范围选择器的当前值（或多个值）。

### min

```tsx
min: number
```
**必填** 范围的最小限制值。

### max

```tsx
max: number
```
**必填** 范围的最大限制值。

### stepSize

```ts
stepSize: number
```
**必填** 可选步长之间的间隔距离。

### onChange

```ts
onChange: (instance: Ranger<TTrackElement>) => void
```
当拖拽手柄释放时触发的回调函数。

## API

### handles
```tsx
handles: ReadonlyArray<{value: number; isActive: boolean; onKeyDownHandler(event): function; onMouseDownHandler(event): function; onTouchStart(event): function}>
```
需要渲染的手柄集合。每个 `handle` 包含以下属性：
 - `value: number` - 手柄当前对应的值
 - `isActive: boolean` - 标识该手柄是否正被拖拽
 - `onKeyDownHandler(event): func`
 - `onMouseDownHandler(event): func`
 - `onTouchStart(event): func`

### activeHandleIndex
```tsx
activeHandleIndex: null | number
```
当前被拖拽手柄的从零开始的索引值，如果没有手柄被拖拽则为 `null`。
