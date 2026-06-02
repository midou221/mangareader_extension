<div dir="rtl">

# مصادر Manga Reader العربية

هذا المستودع يحتوي على قائمة مصادر عربية يمكن إضافتها إلى تطبيق Manga Reader.
ملف المصادر يجب أن يكون بصيغة `List<SourceJsonObject>` حتى يقبله التطبيق.

## الروابط المباشرة

- رابط ملف المصادر الخام:
  [https://raw.githubusercontent.com/midou221/mangareader_extension/main/index.min.json](https://raw.githubusercontent.com/midou221/mangareader_extension/main/index.min.json)

## طريقة إضافة المصادر إلى التطبيق

1. افتح تطبيق قارئ مانجا عربي
2. ادخل إلى صفحة ادارة المصادر.
3. اضغط على زر إضافة مصدر.
4. الصق رابط ملف المصادر الخام. يجب أن ينتهي الرابط بـ `.json`:

```text
https://raw.githubusercontent.com/midou221/mangareader_extension/main/index.min.json
```

5. اضغط حفظ.
6. سيقوم التطبيق بتحميل الملف، فحص المصادر المدعومة، ثم إضافتها إلى المصادر اليدوية.
7. يمكن تحديث المصادر لاحقاً بالسحب للتحديث من صفحة المصادر.

## صيغة ملف index.min.json

الحقول الأساسية هي:

| الحقل | الوصف |
| --- | --- |
| `id` | معرف ثابت للمصدر داخل المستودع |
| `name` | اسم المصدر الذي يظهر للمستخدم |
| `baseUrl` | رابط الموقع الأساسي |
| `sExt` | نوع المزود المستخدم لتشغيل المصدر |
| `listUrl` | اختياري، مسار قائمة الأعمال لبعض المزودات |
| `tagPrefix` | اختياري، بادئة وسوم التصنيف لبعض المزودات |
| `paraWithoutAjax` | اختياري، يستخدم مع بعض مصادر Madara |
| `postreq` | اختياري، عند الحاجة لطلبات POST |
| `useApi` | اختياري، عند الحاجة لاستخدام API |
| `headers` | اختياري، ترويسات HTTP إضافية |
| `msg` | اختياري، رسالة تظهر مع المصدر |

أنواع `sExt` المدعومة:

```text
MAD, Them, GProv, TeamProv, Keyo, Iken, PRO, Swat, Wave, Tek, Time, Zeist
```

مثال مختصر:

```json
[
  {
    "id": "-465016169",
    "name": "مانجا ليك",
    "baseUrl": "https://lek-manga.net",
    "sExt": "MAD",
    "listUrl": "manga/"
  }
]
```

أي ملف JSON عشوائي أو مصدر بنوع `sExt` غير مدعوم سيتم رفضه أثناء الاستيراد.

## المصادر المتوفرة

| المصدر | الرابط |
| --- | --- |
| مانجا ليك | https://lek-manga.net |
| أزورا مانجا | https://azoramoon.com |
| مانجا دايلر | https://dilar.tube |
| تيم إيكس | https://olympustaff.com |
| آريا مانجا | https://ar.kenmanga.com |
| مانجا تايم | https://mangatime.org |
| مانجا تك | https://mangatek.com |
| لافا سكانز | https://lavascans.com |
| مانجا سوات | https://meshmanga.com |
| العاشق | https://3asq.org |
| روكس مانجا | https://rocksmanga.com |
| stellarsaber | https://stellarsaber.pro |
| hijala | https://hijala.com |
| كوميكس فيرس | https://arcomixverse.blogspot.com |

## ملاحظات

- إذا توقف أحد المصادر، قد يكون الموقع غير متاح مؤقتاً أو تغير رابط الموقع.
- يمكن تحديث ملف `index.min.json` في هذا المستودع عند تغيير الروابط أو إضافة مصادر جديدة.
- استخدم رابط الملف الخام دائماً عند الاستيراد، وليس رابط صفحة GitHub العادية.
- لا تغيّر حالة أحرف الرابط؛ مسارات GitHub الخام حساسة لحالة الأحرف.
- كلمة `main` في الرابط هي اسم الفرع في GitHub، لذلك يجب أن يكون `index.min.json` في جذر المستودع.

</div>
