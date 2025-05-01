---
source-updated-at: '2024-01-25T21:28:06.000Z'
translation-updated-at: '2025-05-01T17:34:49.936Z'
name: Logarithmic Interpolator
route: /api/logarithmic-interpolator
menu: API
title: 対数補間 (Logarithmic Interpolator)
---
## 例

実装に直接進みたいですか？以下の例を確認してください:

- [logarithmic-interpolator](../examples/logarithmic-interpolator)

以下のAPIでは、**logarithmic-interpolator** 機能の使用方法について説明します。

## オプション

デフォルトでは、`react-ranger`はデータポイント間の線形補間を使用しますが、以下のインターフェースを実装したオブジェクトを渡すことで、独自の補間関数を簡単にカスタマイズできます。

### interpolator

```tsx
interpolator: {
    getPercentageForValue: (val: number, min: number, max: number): number;
    getValueForClientX: (clientX: number, trackDims: object, min: number, max: number): number;
}
```
使用する補間器 (interpolator)。デフォルトではバンドルされている線形スケール (linear-scale) 補間器を使用します。
 - `getPercentageForValue` - 値と範囲を受け取り、左から右への値の位置を示すパーセンテージ [0, 100] を返します。
 - `getValueForClientX` - clientX（レンジャーの左端からのオフセット）と寸法、範囲設定を受け取り、ピクセル座標を値に変換します。
