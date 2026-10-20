# غلاف PWA لتطبيق «سجل الموظفين»

## الملفات
- `index.html` — صفحة الغلاف: تفتح تطبيق Apps Script بملء الشاشة + شاشة بدء + شاشة «لا يوجد اتصال» + زر التثبيت.
- `manifest.json` — اسم التطبيق وأيقوناته وألوانه ووضع العرض بلا شريط المتصفح.
- `sw.js` — Service Worker: يخزّن الهيكل فقط (لا يخزّن أي بيانات موظفين).
- `icons/` — أيقونات التطبيق.

## النشر على GitHub Pages (مجاناً)
1. أنشئ مستودعاً جديداً على github.com (مثلاً `karmendan`).
2. ارفع محتويات هذا المجلد كما هي (index.html في الجذر).
3. Settings › Pages › Source: `Deploy from a branch` › الفرع `main` › المجلد `/ (root)` › Save.
4. بعد دقيقة يصبح الرابط: `https://<اسم-حسابك>.github.io/karmendan/`

## قبل التجربة
- في Apps Script: استبدل Code.gs بالنسخة الجديدة (فيها `setXFrameOptionsMode(ALLOWALL)`).
- Deploy › Manage deployments › New version.
- يجب أن يكون «Who has access» = **Anyone** (وليس «Anyone with Google account»).
- إذا تغيّر رابط الـ Web app، عدّل `APP_URL` في `index.html`.
- عند تعديل أي ملف هنا، غيّر `VERSION` في `sw.js`.
