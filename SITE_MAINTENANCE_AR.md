# دليل صيانة ونشر موقع Moustafa البحثي

هذا الدليل يحدد الملفات التي تعدّلها عادةً، وطريقة معاينة التغييرات، ثم رفعها إلى GitHub Pages بأقل قدر من المخاطرة.

## 1. أين توجد المعلومات؟

| المطلوب | الملف |
|---|---|
| إضافة بحث منشور أو مخطوط | `_data/publications.yml` |
| تعديل مقدمة الصفحة أو المشروعات أو الأخبار | `_pages/about.md` |
| تعديل Scholar / ORCID / ACL / OpenReview / GitHub / LinkedIn | `_config.yml` داخل `author:` و`social.links:` |
| تعديل صفحة التواصل | `_pages/contact.md` |
| تعديل الألوان والبطاقات والاستجابة للموبايل | `assets/css/main.scss` |
| تعديل شريط التنقل | `_data/navigation.yml` |
| استبدال السيرة الذاتية | `files/Moustafa_Yehia_Hassan_CV.pdf` مع الحفاظ على الاسم نفسه |
| استبدال الصورة الشخصية | `images/avatar.jpg` مع الحفاظ على الاسم نفسه |

## 2. إضافة بحث جديد

افتح `_data/publications.yml` وأضف كتلة جديدة تحت `published:`، مع الالتزام بالمسافات كما في المثال:

```yml
  - title: "Paper title"
    year: "2027"
    status: "Published"
    venue: "Conference or Journal"
    note: "Publisher · pages 1–10"
    summary: >-
      One concise sentence explaining the real contribution.
    links:
      - label: "Paper"
        url: "https://publisher.example/paper"
      - label: "PDF"
        url: "https://publisher.example/paper.pdf"
      - label: "DOI"
        url: "https://doi.org/..."
      - label: "Code"
        url: "https://github.com/..."
```

لا تضف رابطًا غير متاح فعلًا. احذف أي عنصر غير موجود مثل PDF أو DOI بدل ترك رابط وهمي.

لن تحتاج إلى تعديل HTML؛ الصفحة تقرأ الملف تلقائيًا وتبني البطاقة.

## 3. نقل مخطوط من «تحت المراجعة» إلى «منشور»

1. انقل الكتلة من `manuscripts:` إلى `published:`.
2. غيّر `status` إلى `Published`.
3. أضف `venue` و`note` وروابط الناشر/DOI/PDF عند توفرها.
4. عدّل أي خبر أو وصف مكرر في `_pages/about.md`، خصوصًا قسمي **Projects** و**News**.

## 4. تعديل الملفات الأكاديمية

في `_config.yml` ستجد:

```yml
author:
  googlescholar: "..."
  orcid: "..."
  aclanthology: "..."
  openreview: "..."
```

عدّل الرابط هنا مرة واحدة؛ الصفحة الرئيسية وصفحة التواصل والشريط الجانبي ستستخدم القيمة نفسها.

## 5. المسار الآمن للنشر باستخدام PowerShell

قبل التنفيذ، افتح في GitHub: **Settings → Pages → Build and deployment**. تأكد من مصدر النشر الفعلي. الأوامر التالية تفترض أن المصدر هو `main` والمجلد هو `(root)`، وهو الإعداد المعتاد لمستودع مستخدم باسم `myh-ai.github.io`.

نفّذ داخل نسخة Git الحقيقية، لا داخل ملف ZIP فقط:

```powershell
Set-Location "C:\path\to\myh-ai.github.io"
git status
git pull --ff-only origin main
git switch -c site/research-profile-update
```

بعد نسخ الملفات المعدلة إلى الريبو:

```powershell
git status
git diff --check
git diff
```

ثم:

```powershell
git add _config.yml _data/publications.yml _pages/about.md _pages/contact.md `
  _includes/author-profile.html _includes/head/custom.html _includes/masthead.html `
  _includes/footer.html _layouts/default.html assets/css/main.scss README.md SITE_MAINTENANCE_AR.md .gitignore robots.txt

git diff --cached
git commit -m "Add published papers and academic profiles"
git push -u origin site/research-profile-update
```

افتح GitHub وأنشئ Pull Request إلى `main`. افحص تبويب **Checks**، ثم ادمج الطلب. لا تصبح التغييرات منشورة لمجرد إنشاء Pull Request؛ يبدأ نشر الموقع عندما تدخل التغييرات إلى فرع/مجلد النشر المحدد في إعدادات Pages.

### النشر المباشر الأبسط

عندما تكون وحدك على الريبو ومتأكدًا من التغييرات:

```powershell
git switch main
git pull --ff-only origin main
git add .
git diff --cached
git commit -m "Update research portfolio"
git push origin main
```

المسار الأول أكثر أمانًا لأنه يمنحك نقطة مراجعة قبل الدمج.

## 6. المعاينة المحلية على Windows

ثبّت Ruby مع DevKit، ثم داخل الريبو:

```powershell
gem install bundler
bundle config set --local path "vendor/bundle"
bundle install
bundle exec jekyll serve --livereload
```

افتح:

```text
http://127.0.0.1:4000/
```

أوقف الخادم بـ `Ctrl+C`.

## 7. التحقق بعد الرفع

1. افتح تبويب **Actions** وتأكد من نجاح بناء GitHub Pages.
2. افتح **Settings → Pages** وتأكد من حالة النشر.
3. افتح الموقع في نافذة خاصة أو نفّذ تحديثًا قسريًا `Ctrl+F5`.
4. اختبر الصفحة على الكمبيوتر والموبايل والوضع الداكن.
5. افتح روابط ACL وIEEE وScholar وORCID وOpenReview من الموقع نفسه.
6. تأكد من عدم ظهور `404` في روابط الورق أو PDF أو الكود.

## 8. الرجوع السريع عند وجود مشكلة

لم تُدفع التغييرات بعد:

```powershell
git restore .
```

دُفعت في commit منفصل وتريد عكسه بأمان:

```powershell
git log --oneline -5
git revert <commit-sha>
git push origin main
```

استخدم `git revert` على الفرع المنشور، ولا تستخدم `git reset --hard` إلا إذا كنت تفهم أثره تمامًا.
