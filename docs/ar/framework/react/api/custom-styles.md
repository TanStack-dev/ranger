---
source-updated-at: '2024-01-25T21:28:06.000Z'
translation-updated-at: '2025-05-01T17:57:47.133Z'
name: Custom Styles
route: /api/custom-styles
menu: API
title: أنماط مخصصة
---
## أمثلة
هل تريد الانتقال مباشرة إلى التطبيق؟ تحقق من هذه الأمثلة:

- [custom-styles](../examples/custom-styles)

يصف الواجهة البرمجية أدناه كيفية استخدام ميزة **custom-steps**.

## الواجهة البرمجية (API)

### getSegments
```tsx
getSegments: () => ReadonlyArray<{left: number; width: number}>
```
المقاطع (segments) التي سيتم عرضها. يحتوي كل `segment` على الخصائص التالية:
  - `left: number` - قيمة النسبة المئوية لموقع بداية المقطع على أداة المدى (ranger)
  - `width: number` - قيمة النسبة المئوية لعرض المقطع
