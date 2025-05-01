---
source-updated-at: '2024-01-25T21:28:06.000Z'
translation-updated-at: '2025-05-01T17:52:22.258Z'
name: Logarithmic Interpolator
route: /api/logarithmic-interpolator
menu: API
title: Interpolateur logarithmique
---
## Exemples
Vous souhaitez passer directement à l'implémentation ? Consultez ces exemples :

- [logarithmic-interpolator](../examples/logarithmic-interpolator)

L'API ci-dessous décrit comment utiliser les fonctionnalités du **logarithmic-interpolator**.

## Options

Par défaut, `react-ranger` utilise une interpolation linéaire entre les points de données, mais vous permet de facilement personnaliser cette interpolation en utilisant vos propres fonctions en passant un objet qui implémente l'interface suivante.

### interpolator

```tsx
interpolator: {
    getPercentageForValue: (val: number, min: number, max: number): number;
    getValueForClientX: (clientX: number, trackDims: object, min: number, max: number): number;
}
```
L'interpolateur (interpolator) à utiliser. Par défaut, utilise l'interpolateur linéaire intégré.
 - `getPercentageForValue` - Prend la valeur et la plage (range), puis retourne un pourcentage [0, 100] correspondant à la position de la valeur de gauche à droite.
 - `getValueForClientX` - Prend la coordonnée clientX (décalage depuis le bord gauche du ranger) ainsi que les dimensions et les paramètres de plage, puis transforme une coordonnée en pixels en une valeur.
