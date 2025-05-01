---
source-updated-at: '2024-01-25T21:28:06.000Z'
translation-updated-at: '2025-05-01T17:56:50.659Z'
name: Custom Steps
route: /api/custom-steps
menu: API
title: خطوات مخصصة
---
## أمثلة
هل تريد الانتقال مباشرة إلى التنفيذ؟ تحقق من هذه الأمثلة:

- [custom-steps](../examples/custom-steps)

يصف واجهة برمجة التطبيقات (API) أدناه كيفية استخدام ميزات **custom-steps**.

## الخيارات

### steps

```ts
steps: Array<number>
```
مصفوفة من الخطوات المخصصة للاستخدام. سيؤدي هذا إلى تجاوز `stepSize`.

### ticks

```ts
ticks: Array<number>
```
مصفوفة من العلامات المخصصة للاستخدام. سيؤدي هذا إلى تجاوز `tickSize`.

## واجهة برمجة التطبيقات (API)

### getTicks
```tsx
getTicks: () => ReadonlyArray<{value: number; key: number; percentage: number}>
```
العلامات التي سيتم عرضها. يحتوي كل `tick` على الخصائص التالية:
  - `value: number` - رقم العلامة المطلوب عرضه
  - `key: number` - المفتاح الخاص بالعلامة
  - `percentage: number` - القيمة النسبية لمكان وضع العلامة على أداة Ranger
