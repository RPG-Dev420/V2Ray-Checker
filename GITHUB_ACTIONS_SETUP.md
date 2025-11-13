# 🔧 راهنمای فعال‌سازی GitHub Actions

## ⚠️ مشکل: "GitHub Actions is currently disabled for your account"

این پیام به این معنی است که GitHub Actions برای حساب شما یا repository غیرفعال است.

---

## ✅ راه‌حل‌ها

### 1️⃣ فعال‌سازی در سطح Repository

1. **رفتن به Repository Settings**:
   - به repository خود در GitHub بروید
   - روی تب **Settings** کلیک کنید

2. **رفتن به بخش Actions**:
   - در منوی سمت چپ، **Actions** → **General** را انتخاب کنید

3. **فعال‌سازی Actions**:
   - در بخش **Actions permissions**:
     - ✅ **Allow all actions and reusable workflows** را انتخاب کنید
     - یا **Allow local actions and reusable workflows** را انتخاب کنید

4. **ذخیره تغییرات**:
   - روی **Save** کلیک کنید

---

### 2️⃣ بررسی محدودیت‌های حساب

اگر هنوز کار نمی‌کند:

1. **بررسی محدودیت‌های حساب**:
   - Settings → Account → Billing
   - مطمئن شوید که حساب شما محدود نشده است

2. **بررسی Email Verification**:
   - Settings → Emails
   - مطمئن شوید که ایمیل شما تایید شده است

---

### 3️⃣ فعال‌سازی در سطح Organization (اگر repository در Organization است)

اگر repository در یک Organization است:

1. **رفتن به Organization Settings**:
   - به Organization بروید
   - Settings → Actions → General

2. **فعال‌سازی Actions**:
   - **Allow all actions and reusable workflows** را انتخاب کنید

3. **بررسی Policy**:
   - مطمئن شوید که هیچ policy محدودکننده‌ای وجود ندارد

---

### 4️⃣ تماس با GitHub Support

اگر هیچ‌کدام از راه‌حل‌های بالا کار نکرد:

1. **رفتن به GitHub Support**:
   - https://support.github.com/contact
   - یا از طریق: Settings → Account → Support

2. **ارسال درخواست**:
   - موضوع: "GitHub Actions disabled for my account"
   - توضیح دهید که می‌خواهید Actions را فعال کنید
   - Repository URL را ذکر کنید

---

## 🔍 بررسی وضعیت Actions

### بررسی اینکه Actions فعال است یا نه:

1. **رفتن به Actions Tab**:
   - در repository خود، روی تب **Actions** کلیک کنید

2. **مشاهده پیام**:
   - اگر Actions فعال باشد، لیست workflow runs را می‌بینید
   - اگر غیرفعال باشد، پیام "GitHub Actions is currently disabled" را می‌بینید

---

## 📋 Workflow های موجود در این پروژه

بعد از فعال‌سازی Actions، workflow های زیر به صورت خودکار کار می‌کنند:

1. **v2ray-collector.yml** - جمع‌آوری خودکار کانفیگ‌ها (هر 30 دقیقه)
2. **ci.yml** - تست و CI/CD
3. **test.yml** - اجرای تست‌ها
4. **deploy-pages.yml** - Deploy به GitHub Pages
5. **docker-build.yml** - ساخت Docker image
6. **release.yml** - ایجاد Release
7. **security-scan.yml** - اسکن امنیتی
8. **auto-collect.yml** - جمع‌آوری دستی
9. **manual-run.yml** - اجرای دستی

---

## 🚀 تست فعال‌سازی

بعد از فعال‌سازی:

1. **Push یک تغییر کوچک**:
   ```bash
   git commit --allow-empty -m "Test GitHub Actions"
   git push
   ```

2. **بررسی Actions Tab**:
   - باید workflow run جدیدی شروع شود

3. **اجرای دستی**:
   - Actions → انتخاب workflow → Run workflow

---

## ⚙️ تنظیمات پیشنهادی

### در Repository Settings → Actions → General:

- ✅ **Allow all actions and reusable workflows**
- ✅ **Allow GitHub Actions to create and approve pull requests**
- ✅ **Workflow permissions**: Read and write permissions
- ✅ **Allow actions created by GitHub**: فعال

---

## 📞 پشتیبانی

اگر مشکل حل نشد:

1. **GitHub Community Forum**: https://github.community/
2. **GitHub Support**: https://support.github.com/contact
3. **Documentation**: https://docs.github.com/en/actions

---

## ✅ چک‌لیست

- [ ] Actions در Repository Settings فعال است
- [ ] Actions در Organization Settings فعال است (اگر applicable)
- [ ] Email تایید شده است
- [ ] حساب محدود نشده است
- [ ] Workflow files در `.github/workflows/` وجود دارند
- [ ] Syntax workflow files صحیح است

---

**💡 نکته**: بعد از فعال‌سازی، ممکن است چند دقیقه طول بکشد تا Actions شروع به کار کند.

