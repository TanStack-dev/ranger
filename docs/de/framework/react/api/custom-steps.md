---
source-updated-at: '2024-01-25T21:28:06.000Z'
translation-updated-at: '2025-05-01T17:50:52.932Z'
name: Custom Steps
route: /api/custom-steps
menu: API
title: Benutzerdefinierte Schritte
---
## Beispiele  
Möchten Sie direkt zur Implementierung springen? Sehen Sie sich diese Beispiele an:  

- [custom-steps](../examples/custom-steps)  

Die folgende API beschreibt, wie die **custom-steps**-Funktionen verwendet werden.  

## Optionen  

### steps  

```ts  
steps: Array<number>  
```  
Ein Array benutzerdefinierter Schritte. Dadurch wird `stepSize` überschrieben.  

### ticks  

```ts  
ticks: Array<number>  
```  
Ein Array benutzerdefinierter Ticks. Dadurch wird `tickSize` überschrieben.  

## API  

### getTicks  
```tsx  
getTicks: () => ReadonlyArray<{value: number; key: number; percentage: number}>  
```  
Ticks, die gerendert werden sollen. Jeder `tick` hat die folgenden Eigenschaften:  
  - `value: number` – Die anzuzeigende Tick-Nummer  
  - `key: number` – Der Schlüssel eines Ticks  
  - `percentage: number` – Prozentualer Wert, der angibt, wo der Tick auf dem Ranger platziert werden soll
