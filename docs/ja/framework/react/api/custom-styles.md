---
source-updated-at: '2024-01-25T21:28:06.000Z'
translation-updated-at: '2025-05-01T17:34:35.952Z'
name: Custom Styles
route: /api/custom-styles
menu: API
title: カスタムスタイル
---
## 例
実装に直接進みたいですか？以下の例を確認してください:

- [custom-styles](../examples/custom-styles)

以下のAPIでは、**custom-steps**機能の使用方法について説明しています。

## API

### getSegments
```tsx
getSegments: () => ReadonlyArray<{left: number; width: number}>
```
レンダリングするセグメント。各`segment`は以下のプロパティを持ちます:
  - `left: number` - レンジャー上でセグメントが開始する位置のパーセンテージ値
  - `width: number` - セグメントの幅のパーセンテージ値
