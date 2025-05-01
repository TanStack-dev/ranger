---
source-updated-at: '2024-01-25T21:28:06.000Z'
translation-updated-at: '2025-05-01T17:34:26.712Z'
name: Custom Steps
route: /api/custom-steps
menu: API
title: カスタムステップ
---
## 例
実装をすぐに確認したいですか？以下の例をご覧ください:

- [custom-steps](../examples/custom-steps)

以下のAPIでは、**custom-steps**機能の使用方法について説明しています。

## オプション

### steps

```ts
steps: Array<number>
```
使用するカスタムステップの配列。`stepSize`を上書きします。

### ticks

```ts
ticks: Array<number>
```
使用するカスタムティックの配列。`tickSize`を上書きします。

## API

### getTicks
```tsx
getTicks: () => ReadonlyArray<{value: number; key: number; percentage: number}>
```
レンダリングするティック。各`tick`には以下のプロパティがあります:
  - `value: number` - 表示するティックの数値
  - `key: number` - ティックのキー
  - `percentage: number` - レンジャー上にティックを配置する位置のパーセンテージ値
