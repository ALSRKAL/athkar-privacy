# خطوات نشر صفحات الخصوصية على GitHub Pages

## الخطوة 1: إنشاء مستودع على GitHub
1. اذهب إلى https://github.com/new
2. أنشئ مستودع جديد باسم `athkar-privacy` (أو أي اسم تريده)
3. اختر **Public** (مطلوب لـ GitHub Pages المجاني)

## الخطوة 2: رفع الملفات
```bash
cd docs
git init
git add .
git commit -m "Add privacy policy and terms"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/athkar-privacy.git
git push -u origin main
```

## الخطوة 3: تفعيل GitHub Pages
1. اذهب إلى إعدادات المستودع (Settings)
2. في القائمة الجانبية، اختر **Pages**
3. في قسم **Source**، اختر:
   - Branch: `main`
   - Folder: `/ (root)`
4. اضغط **Save**

## الخطوة 4: احصل على الروابط
بعد دقائق قليلة، ستكون الصفحات متاحة على:
- **الرئيسية**: `https://YOUR_USERNAME.github.io/athkar-privacy/`
- **سياسة الخصوصية**: `https://YOUR_USERNAME.github.io/athkar-privacy/privacy.html`
- **شروط الاستخدام**: `https://YOUR_USERNAME.github.io/athkar-privacy/terms.html`

## الخطوة 5: تحديث التطبيق
قم بتحديث رابط سياسة الخصوصية في التطبيق:
`lib/presentation/screens/settings/settings_screen.dart`

استبدل:
```dart
const privacyUrl = 'https://sites.google.com/view/athkar-privacy-policy';
```
بـ:
```dart
const privacyUrl = 'https://YOUR_USERNAME.github.io/athkar-privacy/privacy.html';
```
