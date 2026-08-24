# 🚀 GitHub Actions Telegram Bot Automation

مجلد جاهز ومستقل يحتوي على جميع الملفات الخاصة برفع وتفعيل أتمتة إرسال تقارير التلغرام عبر **GitHub Actions**.

---

## 📁 محتويات المجلد:

1. **`send_attendance_telegram.py`**: سكريبت البايثون الذي يقرأ التواريخ المجدولة من Supabase، ينشئ ملفات الـ PDF، يرسلها للتلغرام، ويمسح التواريخ أوتوماتيكياً.
2. **`requirements.txt`**: قائمة المكتبات المطلوبة لتشغيل البايثون.
3. **`.github/workflows/send_telegram_reports.yml`**: ملف أتمتة GitHub Actions للتشغيل التلقائي عبر إشارة الموقع أو الجدول الزمني.

---

## ⚙️ خطوات التفعيل على GitHub:

### 1. رفع المجلد إلى مستودع GitHub الخاص بك
قم بإنشاء Repository جديد على GitHub وارفع فيه محتويات هذا المجلد:
```bash
git init
git add .
git commit -m "Add Telegram Bot GitHub Actions Workflow"
git branch -M main
git remote add origin https://github.com/USERNAME/REPO-NAME.git
git push -u origin main
```

---

### 2. إضافة الـ Secrets في GitHub
اذهب إلى مستودعك على GitHub:
👈 **Settings** ➔ **Secrets and variables** ➔ **Actions** ➔ اضغط **New repository secret** وأضف المتغيرات التالية:

| اسم السري (Secret Name) | القيمة (Value) |
|---|---|
| `TELEGRAM_BOT_TOKEN` | التوكن الخاص ببوت التلغرام (مثال: `7914915084:...`) |
| `TELEGRAM_CHAT_ID` | معرف المجموعة (مثال: `-1002697037825`) |
| `NEXT_PUBLIC_SUPABASE_URL` | `https://qjzrdsvtjdjvnvpusbbi.supabase.co` |
| `NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY` | `sb_publishable_adEGsCZFyrnoiu7g-IZ6Gg_vowP7cPU` |

---

### 3. ربطه بالموقع الإلكتروني
في ملف `.env` الخاص بموقعك الرئيسي، أضف السطرين التاليين لتشغيل الـ GitHub Action بنقرة زر من الـ Dashboard:
```env
GITHUB_REPO=USERNAME/REPO-NAME
GITHUB_PAT=ghp_your_personal_access_token
```

جاهز 100%! 🚀
