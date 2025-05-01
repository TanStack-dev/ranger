---
source-updated-at: '2024-01-25T21:28:06.000Z'
translation-updated-at: '2025-05-01T17:55:43.351Z'
name: Custom Steps
route: /api/custom-steps
menu: API
title: Пользовательские шаги
---
## Примеры
Хотите сразу перейти к реализации? Ознакомьтесь с этими примерами:

- [custom-steps](../examples/custom-steps)

В API ниже описано, как использовать возможности **custom-steps**.

## Опции

### steps

```ts
steps: Array<number>
```
Массив пользовательских шагов (steps). Переопределяет `stepSize`.

### ticks

```ts
ticks: Array<number>
```
Массив пользовательских отметок (ticks). Переопределяет `tickSize`.

## API

### getTicks
```tsx
getTicks: () => ReadonlyArray<{value: number; key: number; percentage: number}>
```
Отметки (ticks) для рендеринга. Каждая `tick` содержит следующие свойства:
  - `value: number` — Числовое значение отметки для отображения
  - `key: number` — Уникальный ключ отметки
  - `percentage: number` — Процентное значение позиции отметки на шкале (ranger)
