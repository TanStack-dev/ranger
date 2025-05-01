---
source-updated-at: '2024-01-25T21:28:06.000Z'
translation-updated-at: '2025-05-01T17:51:20.954Z'
name: Custom Styles
route: /api/custom-styles
menu: API
title: Benutzerdefinierte Stile
---
## Beispiele
Möchten Sie direkt zur Implementierung springen? Sehen Sie sich diese Beispiele an:

- [custom-styles](../examples/custom-styles)

Die folgende API beschreibt, wie die **custom-steps**-Funktionen verwendet werden.

## API

### getSegments
```tsx
getSegments: () => ReadonlyArray<{left: number; width: number}>
```
Segmente, die gerendert werden sollen. Jedes `segment` hat die folgenden Eigenschaften:
  - `left: number` - Prozentualer Wert, wo das Segment auf dem Ranger beginnen soll  
  - `width: number` - Prozentualer Wert der Segmentbreite
