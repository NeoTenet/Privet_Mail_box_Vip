<p align="center">
  <img src="./banner.jpg" alt="Neo Box Panel" width="100%">
</p>

<h1 align="center">📬 Neo Box Panel</h1>

<p align="center">
  <strong>پنل دریافت ایمیل روی دامنه شخصی</strong><br>
  <em>Personal email inbox on your own domain</em>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Version-2.0-blueviolet" alt="v">
  <img src="https://img.shields.io/badge/Receive-Only-orange" alt="recv">
  <img src="https://img.shields.io/badge/Cloudflare-Worker-F38020" alt="cf">
</p>

<p align="center">
  <a href="#-فارسی">🇮🇷 فارسی</a> ·
  <a href="#-english">🇬🇧 English</a>
</p>

---

# 🇮🇷 فارسی

## معرفی

**Neo Box Panel** پنل وب برای **دریافت ایمیل** روی دامنه خودتان است.  
دامنه اصلی و زیردامنه‌های فیک را مدیریت می‌کنید و همه پیام‌ها در یک صندوق جمع می‌شوند.

> فقط **دریافت** ایمیل — برای ارسال از جیمیل یا سرویس دیگر استفاده کنید.  
> کپی بدون ذکر منبع اصلی مجاز نیست.

---

## دانلود کد

کد `worker.js` در شاخه اصلی نیست.

1. برو **Releases**
2. نسخه `v2.0` را باز کن
3. فایل `worker.js` را دانلود کن

---

## پیش‌نمایش

### دسکتاپ — شب

![دسکتاپ شب](./screenshots/desktop-dark.jpg)

### دسکتاپ — روز

![دسکتاپ روز](./screenshots/desktop-light.jpg)

### موبایل

| شب | روز |
|----|-----|
| ![موبایل شب](./screenshots/mobile-dark.jpg) | ![موبایل روز](./screenshots/mobile-light.jpg) |

### دامنه‌ها

![دامنه‌ها](./screenshots/domains-modal.jpg)

---

## راه‌اندازی

### پیش‌نیاز
دامنه روی Cloudflare (Nameserverها روی Cloudflare)

### ۱) دیتابیس D1
Storage & Databases → D1 → Create → نام: `postbox`

### ۲) Worker
Workers & Pages → Create Worker → `postbox` → Deploy  
Edit code → پیست `worker.js` → Deploy

### ۳) Binding
Settings → Bindings → D1 → Variable name: **`DB`**

### ۴) متغیرها

| نام | نوع |
|-----|------|
| `PANEL_PASSWORD` | Secret |
| `MAIN_DOMAIN` | Text |
| `CF_ZONE_ID` | Text |
| `CF_API_TOKEN` | Secret |

### ۵) Email Routing
Email → Email Routing → Enable  
Catch-all → Send to Worker → `postbox`

### ۶) آدرس پنل
Domains & Routes → **Add Domain** (نه Add Route)  
مثال: `panel.example.com`

### ۷) تست
ورود → دامنه‌ها → ساخت دامنه فیک → ارسال ایمیل تست

---

## نسخه ۲.۰

- نام: Neo Box Panel  
- ۳ تم رنگی + عنوان طلایی  
- مودال دامنه‌ها  
- منوی موبایل پایین صفحه  
- رفع باگ UI  

---

## سازنده

**NeoTenet**

- [t.me/neotenet](https://t.me/neotenet)  
- [github.com/NeoTenet](https://github.com/NeoTenet)  
- [youtube.com/@Neo_Tenet](https://www.youtube.com/@Neo_Tenet)

---

# 🇬🇧 English

**Neo Box Panel** — receive-only personal email panel for your domain.

Download `worker.js` from **Releases** (not the main branch).

Setup: D1 `postbox` → Worker → bind **`DB`** → secrets → Email Routing catch-all → **Add Domain**.

Author: **NeoTenet** · Version **2.0**
