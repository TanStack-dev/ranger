---
source-updated-at: '2024-01-25T21:28:06.000Z'
translation-updated-at: '2025-05-01T17:51:38.252Z'
name: Basic
route: /api/basic
menu: API
title: Grundlagen
---
## Beispiele  
Möchten Sie direkt zur Implementierung springen? Hier finden Sie einige Beispiele:

- [basic](../../examples/react/basic)

Die folgende API beschreibt, wie die **grundlegenden** Funktionen verwendet werden.

## Optionen

### values

```tsx
values: ReadonlyArray<number>
```
**Erforderlich** Der aktuelle Wert (oder die Werte) für den Bereich.

### min

```tsx
min: number
```
**Erforderlich** Die untere Grenze für den Bereich.

### max

```tsx
max: number
```
**Erforderlich** Die obere Grenze für den Bereich.

### stepSize

```ts
stepSize: number
```
**Erforderlich** Der Abstand zwischen auswählbaren Schritten.

### onChange

```ts
onChange: (instance: Ranger<TTrackElement>) => void
```
Eine Funktion, die aufgerufen wird, wenn der Handle losgelassen wird.

## API

### handles
```tsx
handles: ReadonlyArray<{value: number; isActive: boolean; onKeyDownHandler(event): function; onMouseDownHandler(event): function; onTouchStart(event): function}>
```
Handles, die gerendert werden sollen. Jeder `handle` hat die folgenden Eigenschaften:
 - `value: number` - Der aktuelle Wert des Handles.
 - `isActive: boolean` - Gibt an, ob der Handle gerade gezogen wird.
 - `onKeyDownHandler(event): func`
 - `onMouseDownHandler(event): func`
 - `onTouchStart(event): func`

### activeHandleIndex
```tsx
activeHandleIndex: null | number
```
Der nullbasierte Index des Handles, der gerade gezogen wird, oder `null`, wenn kein Handle gezogen wird.
