---
source-updated-at: '2024-01-25T21:28:06.000Z'
translation-updated-at: '2025-05-01T17:54:29.757Z'
name: Basic
route: /api/basic
menu: API
title: Базовый
---
## Примеры
Хотите сразу перейти к реализации? Ознакомьтесь с этими примерами:

- [basic](../../examples/react/basic)

В API ниже описаны основные возможности.

## Опции

### values

```tsx
values: ReadonlyArray<number>
```
**Обязательный параметр** Текущее значение (или значения) диапазона.

### min

```tsx
min: number
```
**Обязательный параметр** Минимальное ограничение для диапазона.

### max

```tsx
max: number
```
**Обязательный параметр** Максимальное ограничение для диапазона.

### stepSize

```ts
stepSize: number
```
**Обязательный параметр** Расстояние между выбираемыми шагами.

### onChange

```ts
onChange: (instance: Ranger<TTrackElement>) => void
```
Функция, вызываемая при отпускании ползунка (handle).

## API

### handles
```tsx
handles: ReadonlyArray<{value: number; isActive: boolean; onKeyDownHandler(event): function; onMouseDownHandler(event): function; onTouchStart(event): function}>
```
Ползунки (handles) для отображения. Каждый `handle` имеет следующие свойства:
 - `value: number` - Текущее значение ползунка.
 - `isActive: boolean` - Указывает, перетаскивается ли ползунок в данный момент.
 - `onKeyDownHandler(event): func`
 - `onMouseDownHandler(event): func`
 - `onTouchStart(event): func`

### activeHandleIndex
```tsx
activeHandleIndex: null | number
```
Индекс (начиная с нуля) ползунка, который перетаскивается в данный момент, или `null`, если ни один ползунок не перетаскивается.
