# 🚀 SmartDownloader

یک GitHub Action هوشمند برای دانلود خودکار فایل‌ها با قابلیت سازماندهی بر اساس نوع فایل

## ✨ قابلیت‌ها

- 📥 دانلود از طریق **Run workflow** (بدون نیاز به commit)
- 📝 دانلود خودکار از **commit message**
- 🗂️ سازماندهی هوشمند فایل‌ها (apk, zip, pdf, mp4, exe و...)
- 📦 حالت فشرده‌سازی (zip)
- ⚡ پشتیبانی از چندین لینک همزمان

## 🎯 روش استفاده

### 1️⃣ استفاده سریع (دستی)
به بخش **Actions** رفته و روی **Run workflow** کلیک کنید:
```yaml
Manual download URL: https://example.com/file.apk
Download mode: normal
```
### 2️⃣   استفاده خودکار
در پیام commit خود بنویسید:
```yaml
git commit -m "download: https://example.com/file.zip"
git commit -m "download-zip: https://example.com/file.pdf"
```

📂 ساختار خروجی
فایل‌ها بر اساس پسوند در پوشه‌های زیر ذخیره می‌شوند:

downloads/apk_files/ - فایل‌های اندروید

downloads/archives/ - فایل‌های فشرده

downloads/documents/ - PDF, DOC, ...

downloads/installers/ - EXE, DEB, ...

downloads/images/ - عکس‌ها

downloads/videos/ - ویدیوها

downloads/others/ - سایر فایل‌ها


📝 مثال
### دانلود یک فایل معمولی
```yaml
download: https://github.com/user/repo/releases/download/v1.0/app.apk
```
### دانلود و فشرده‌سازی
```yaml
download-zip: https://example.com/document.pdf https://example.com/image.jpg
```

⚙️ پیش‌نیازها

فقط کافی است این فایل را در مسیر 
``` .github/workflows/download.yml ```
قرار دهید.
