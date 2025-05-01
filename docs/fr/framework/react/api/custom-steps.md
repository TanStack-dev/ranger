---
source-updated-at: '2024-01-25T21:28:06.000Z'
translation-updated-at: '2025-05-01T17:53:12.958Z'
name: Custom Steps
route: /api/custom-steps
menu: API
title: Pas personnalisés
---
## Exemples
Vous souhaitez passer directement à l'implémentation ? Consultez ces exemples :

- [custom-steps](../examples/custom-steps)

L'API ci-dessous décrit comment utiliser les fonctionnalités **custom-steps**.

## Options

### steps

```ts
steps: Array<number>
```
Un tableau d'étapes personnalisées à utiliser. Cela remplacera `stepSize`.

### ticks

```ts
ticks: Array<number>
```
Un tableau de marqueurs personnalisés à utiliser. Cela remplacera `tickSize`.

## API

### getTicks
```tsx
getTicks: () => ReadonlyArray<{value: number; key: number; percentage: number}>
```
Marqueurs à afficher. Chaque `tick` possède les propriétés suivantes :
  - `value: number` - Le numéro du marqueur à afficher
  - `key: number` - La clé d'un marqueur
  - `percentage: number` - Valeur en pourcentage indiquant où placer le marqueur sur le ranger
