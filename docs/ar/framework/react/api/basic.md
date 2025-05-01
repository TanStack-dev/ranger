---
source-updated-at: '2024-01-25T21:28:06.000Z'
translation-updated-at: '2025-05-01T17:56:27.678Z'
name: Basic
route: /api/basic
menu: API
title: أساسي
---
## أمثلة
هل تريد الانتقال مباشرة إلى التنفيذ؟ تحقق من هذه الأمثلة:

- [basic](../../examples/react/basic)

يصف واجهة برمجة التطبيقات (API) أدناه كيفية استخدام الميزات **الأساسية**.

## الخيارات

### القيم (values)

```tsx
values: ReadonlyArray<number>
```
**مطلوب** القيمة الحالية (أو القيم) للنطاق.

### الحد الأدنى (min)

```tsx
min: number
```
**مطلوب** الحد الأدنى المسموح به للنطاق.

### الحد الأقصى (max)

```tsx
max: number
```
**مطلوب** الحد الأقصى المسموح به للنطاق.

### حجم الخطوة (stepSize)

```ts
stepSize: number
```
**مطلوب** المسافة بين الخطوات القابلة للتحديد.

### عند التغيير (onChange)

```ts
onChange: (instance: Ranger<TTrackElement>) => void
```
دالة يتم استدعاؤها عند تحرير المقبض (handle).

## واجهة برمجة التطبيقات (API)

### المقابض (handles)

```tsx
handles: ReadonlyArray<{value: number; isActive: boolean; onKeyDownHandler(event): function; onMouseDownHandler(event): function; onTouchStart(event): function}>
```
المقابض التي يجب عرضها. يحتوي كل `مقبض (handle)` على الخصائص التالية:
 - `القيمة (value): number` - القيمة الحالية للمقبض.
 - `نشط (isActive): boolean` - يشير إلى ما إذا كان المقبض يتم سحبه حاليًا.
 - `معالج الضغط على المفتاح (onKeyDownHandler)(event): func`
 - `معالج الضغط بالفأرة (onMouseDownHandler)(event): func`
 - `معالج اللمس (onTouchStart)(event): func`

### فهرس المقبض النشط (activeHandleIndex)

```tsx
activeHandleIndex: null | number
```
فهرس المقبض الذي يتم سحبه حاليًا (بدءًا من الصفر)، أو `null` إذا لم يتم سحب أي مقبض.
