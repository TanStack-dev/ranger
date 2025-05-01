---
source-updated-at: '2024-01-25T21:28:06.000Z'
translation-updated-at: '2025-05-01T17:55:52.145Z'
name: Custom Styles
route: /api/custom-styles
menu: API
title: Пользовательские стили
---
## Примеры
Хотите сразу перейти к реализации? Ознакомьтесь с этими примерами:

- [custom-styles](../examples/custom-styles)

API ниже описывает, как использовать функционал **custom-steps**.

## API

### getSegments
```tsx
getSegments: () => ReadonlyArray<{left: number; width: number}>
```
Сегменты для рендеринга. Каждый `segment` имеет следующие свойства:
  - `left: number` - Процентное значение, определяющее начало сегмента на ranger
  - `width: number` - Процентное значение ширины сегмента
