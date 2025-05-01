---
source-updated-at: '2024-01-25T21:28:06.000Z'
translation-updated-at: '2025-05-01T17:51:12.339Z'
name: Logarithmic Interpolator
route: /api/logarithmic-interpolator
menu: API
title: Logarithmischer Interpolator
---
## Beispiele  
Möchten Sie direkt zur Implementierung springen? Sehen Sie sich diese Beispiele an:  

- [logarithmic-interpolator](../examples/logarithmic-interpolator)  

Die folgende API beschreibt, wie Sie die Funktionen des **logarithmic-interpolator** nutzen können.  

## Optionen  

Standardmäßig verwendet `react-ranger` eine lineare Interpolation zwischen Datenpunkten, ermöglicht es Ihnen jedoch, diese einfach anzupassen, indem Sie ein Objekt übergeben, das die folgende Schnittstelle implementiert.  

### interpolator  

```tsx
interpolator: {
    getPercentageForValue: (val: number, min: number, max: number): number;
    getValueForClientX: (clientX: number, trackDims: object, min: number, max: number): number;
}
```  
Der zu verwendende Interpolator (Interpolator). Standardmäßig wird der gebündelte lineare Interpolator (linear-scale interpolator) verwendet.  
 - `getPercentageForValue` - Nimmt den Wert und den Bereich entgegen und gibt einen Prozentsatz [0, 100] zurück, der angibt, wo der Wert von links nach rechts positioniert ist.  
 - `getValueForClientX` - Nimmt die clientX (Offset vom linken Rand des Rangers) zusammen mit den Dimensionen und Bereichseinstellungen entgegen und wandelt eine Pixelkoordinate zurück in einen Wert.
