---
source-updated-at: '2023-12-13T01:26:36.000Z'
translation-updated-at: '2025-05-01T17:53:43.782Z'
title: Démarrage rapide
---
# Démarrage rapide

Si vous êtes impatient et préférez passer outre notre excellente documentation, voici le strict minimum pour commencer avec TanStack Ranger. Nous utiliserons React pour cet exemple, mais les mêmes principes s'appliquent aux autres frameworks.

```tsx
import React from 'react'
import ReactDOM from 'react-dom'
import { useRanger, Ranger } from '@tanstack/react-ranger'

function App() {
  const rangerRef = React.useRef<HTMLDivElement>(null)
  const [values, setValues] = React.useState<ReadonlyArray<number>>([
    10, 15, 50,
  ])

  const rangerInstance = useRanger<HTMLDivElement>({
    getRangerElement: () => rangerRef.current,
    values,
    min: 0,
    max: 100,
    stepSize: 5,
    onChange: (instance: Ranger<HTMLDivElement>) =>
      setValues(instance.sortedValues),
  })

  return (
    <div className="App" style={{ padding: 10 }}>
      <h1>Basic Range</h1>
      <span>Active Index: {rangerInstance.activeHandleIndex}</span>
      <br />
      <br />
      <div
        ref={rangerRef}
        style={{
          position: 'relative',
          userSelect: 'none',
          height: '4px',
          background: '#ddd',
          boxShadow: 'inset 0 1px 2px rgba(0,0,0,.6)',
          borderRadius: '2px',
        }}
      >
        {rangerInstance
          .handles()
          .map(
            (
              {
                value,
                onKeyDownHandler,
                onMouseDownHandler,
                onTouchStart,
                isActive,
              },
              i,
            ) => (
              <button
                key={i}
                onKeyDown={onKeyDownHandler}
                onMouseDown={onMouseDownHandler}
                onTouchStart={onTouchStart}
                role="slider"
                aria-valuemin={rangerInstance.options.min}
                aria-valuemax={rangerInstance.options.max}
                aria-valuenow={value}
                style={{
                  position: 'absolute',
                  top: '50%',
                  left: `${rangerInstance.getPercentageForValue(value)}%`,
                  zIndex: isActive ? '1' : '0',
                  transform: 'translate(-50%, -50%)',
                  width: '14px',
                  height: '14px',
                  outline: 'none',
                  borderRadius: '100%',
                  background: 'linear-gradient(to bottom, #eee 45%, #ddd 55%)',
                  border: 'solid 1px #888',
                }}
              />
            ),
          )}
      </div>
      <br />
      <br />
      <br />
      <pre
        style={{
          display: 'inline-block',
          textAlign: 'left',
        }}
      >
        <code>
          {JSON.stringify({
            values,
          })}
        </code>
      </pre>
    </div>
  )
}

ReactDOM.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>,
  document.getElementById('root'),
)
```

Si vous avez survolé cet exemple ou si quelque chose n'est pas clair, nous ne vous en voulons pas, car il y a tellement plus à apprendre pour vraiment tirer parti de TanStack Ranger ! Continuons.
