---
source-updated-at: '2023-12-13T01:26:36.000Z'
translation-updated-at: '2025-05-01T17:47:15.347Z'
title: 快速開始
---
# 快速開始

如果你感到不耐煩，想跳過我們精彩的說明文件，以下是使用 TanStack Ranger 的最低需求範例。我們將使用 React 作為範例，但相同原則也適用於其他框架。

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

如果你跳過了這個範例或有不理解的地方，我們不會責怪你，因為要真正發揮 TanStack Ranger 的優勢，還有很多需要學習！讓我們繼續前進。
