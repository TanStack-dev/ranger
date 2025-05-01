---
source-updated-at: '2024-01-25T21:28:06.000Z'
translation-updated-at: '2025-05-01T17:52:35.708Z'
name: Custom Styles
route: /api/custom-styles
menu: API
title: Styles personnalisés
---
## Exemples
Vous souhaitez passer directement à l'implémentation ? Consultez ces exemples :

- [custom-styles](../examples/custom-styles)

L'API ci-dessous décrit comment utiliser les fonctionnalités **custom-steps**.

## API

### getSegments
```tsx
getSegments: () => ReadonlyArray<{left: number; width: number}>
```
Segments à afficher. Chaque `segment` possède les propriétés suivantes :
  - `left: number` - Valeur en pourcentage indiquant où le segment doit commencer sur le ranger
  - `width: number` - Valeur en pourcentage de la largeur du segment
