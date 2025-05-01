---
source-updated-at: '2024-01-25T21:28:06.000Z'
translation-updated-at: '2025-05-01T17:53:01.009Z'
name: Basic
route: /api/basic
menu: API
title: Basique
---
## Exemples
Vous souhaitez passer directement à l'implémentation ? Consultez ces exemples :

- [basic](../../examples/react/basic)

L'API ci-dessous décrit comment utiliser les fonctionnalités **de base**.

## Options

### values

```tsx
values: ReadonlyArray<number>
```
**Obligatoire** La ou les valeurs actuelles pour la plage.

### min

```tsx
min: number
```
**Obligatoire** La limite minimale de la plage.

### max

```tsx
max: number
```
**Obligatoire** La limite maximale de la plage.

### stepSize

```ts
stepSize: number
```
**Obligatoire** L'écart entre les étapes sélectionnables.

### onChange

```ts
onChange: (instance: Ranger<TTrackElement>) => void
```
Une fonction appelée lorsque la poignée est relâchée.

## API

### handles
```tsx
handles: ReadonlyArray<{value: number; isActive: boolean; onKeyDownHandler(event): function; onMouseDownHandler(event): function; onTouchStart(event): function}>
```
Poignées à afficher. Chaque `handle` possède les propriétés suivantes :
 - `value: number` - La valeur actuelle de la poignée.
 - `isActive: boolean` - Indique si la poignée est actuellement en cours de déplacement.
 - `onKeyDownHandler(event): func`
 - `onMouseDownHandler(event): func`
 - `onTouchStart(event): func`

### activeHandleIndex
```tsx
activeHandleIndex: null | number
```
L'index (base zéro) de la poignée actuellement en cours de déplacement, ou `null` si aucune poignée n'est déplacée.
