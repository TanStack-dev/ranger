---
source-updated-at: '2024-01-25T21:28:06.000Z'
translation-updated-at: '2025-05-01T17:55:31.158Z'
name: Logarithmic Interpolator
route: /api/logarithmic-interpolator
menu: API
title: Логарифмический интерполятор
---
## Примеры
Хотите сразу перейти к реализации? Ознакомьтесь с этими примерами:

- [logarithmic-interpolator](../examples/logarithmic-interpolator)

API ниже описывает, как использовать возможности **logarithmic-interpolator**.

## Настройки

По умолчанию `react-ranger` использует линейную интерполяцию между точками данных, но позволяет легко настроить её, передав объект, реализующий следующий интерфейс.

### interpolator

```tsx
interpolator: {
    getPercentageForValue: (val: number, min: number, max: number): number;
    getValueForClientX: (clientX: number, trackDims: object, min: number, max: number): number;
}
```
Интерполятор (interpolator) для использования. По умолчанию используется встроенный линейный интерполятор (linear-scale interpolator).
 - `getPercentageForValue` — Принимает значение и диапазон, возвращает процент [0, 100], указывающий положение значения слева направо.
 - `getValueForClientX` — Принимает clientX (смещение от левого края ranger), а также размеры и настройки диапазона, преобразуя координату в пикселях обратно в значение.
