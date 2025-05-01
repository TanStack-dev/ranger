---
source-updated-at: '2024-01-25T21:28:06.000Z'
translation-updated-at: '2025-05-01T17:58:01.673Z'
name: Logarithmic Interpolator
route: /api/logarithmic-interpolator
menu: API
title: المقحم اللوغاريتمي
---
## أمثلة
هل تريد الانتقال مباشرة إلى التنفيذ؟ تحقق من هذه الأمثلة:

- [logarithmic-interpolator](../examples/logarithmic-interpolator)

يصف API أدناه كيفية استخدام ميزات **logarithmic-interpolator**.

## الخيارات

بشكل افتراضي، يستخدم `react-ranger` الاستيفاء الخطي بين نقاط البيانات، ولكنه يسمح لك بتخصيصه بسهولة لاستخدام دوال الاستيفاء الخاصة بك عن طريق تمرير كائن ينفذ الواجهة التالية.

### interpolator

```tsx
interpolator: {
    getPercentageForValue: (val: number, min: number, max: number): number;
    getValueForClientX: (clientX: number, trackDims: object, min: number, max: number): number;
}
```
المستوفي (interpolator) المستخدم. الافتراضي هو مستوفي linear-scale المدمج.
 - `getPercentageForValue` - يأخذ القيمة والنطاق ويعيد النسبة المئوية [0, 100] حيث تقع القيمة من اليسار إلى اليمين.
 - `getValueForClientX` - يأخذ clientX (الإزاحة من الحافة اليسرى لـ ranger) مع الأبعاد وإعدادات النطاق ويحول إحداثيات البكسل مرة أخرى إلى قيمة.
