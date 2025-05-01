---
source-updated-at: '2024-01-25T21:28:06.000Z'
translation-updated-at: '2025-05-01T17:34:09.785Z'
name: Basic
route: /api/basic
menu: API
title: 基本
---
## 例

実装に直接進みたいですか？以下の例を確認してください：

- [basic](../../examples/react/basic)

以下のAPIでは、**basic**機能の使用方法について説明しています。

## オプション

### values

```tsx
values: ReadonlyArray<number>
```
**必須** 範囲の現在の値（または値の配列）。

### min

```tsx
min: number
```
**必須** 範囲の最小限界値。

### max

```tsx
max: number
```
**必須** 範囲の最大限界値。

### stepSize

```ts
stepSize: number
```
**必須** 選択可能なステップ間の距離。

### onChange

```ts
onChange: (instance: Ranger<TTrackElement>) => void
```
ハンドルがリリースされた時に呼び出される関数。

## API

### handles
```tsx
handles: ReadonlyArray<{value: number; isActive: boolean; onKeyDownHandler(event): function; onMouseDownHandler(event): function; onTouchStart(event): function}>
```
レンダリングするハンドル。各`handle`には以下のプロパティがあります：
 - `value: number` - ハンドルの現在の値。
 - `isActive: boolean` - ハンドルが現在ドラッグ中かどうかを示す。
 - `onKeyDownHandler(event): func`
 - `onMouseDownHandler(event): func`
 - `onTouchStart(event): func`

### activeHandleIndex
```tsx
activeHandleIndex: null | number
```
現在ドラッグ中のハンドルのゼロベースのインデックス、またはドラッグ中のハンドルがない場合は`null`。
