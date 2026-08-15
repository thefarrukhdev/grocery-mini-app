# Telegram Grocery Ordering System (v2)

Telegram platformasidagi do'konlar va mijozlar uchun mo'ljallangan, vazn yoki hajm (kg, litr) bo'yicha sotiladigan oziq-ovqat mahsulotlarini buyurtma qilish va boshqarish tizimi (Telegram Mini App).

## 📱 Loyiha Tuzilishi

Loyiha bitta Telegram bot orqali ishga tushadigan ikkita alohida interfeysdan iborat:

1. **Mijoz Mini App (Customer App):** Mahsulotlarni ko'rish, savatcha yig'ish, buyurtma berish va uning holatini kuzatish.
2. **Admin Mini App (Admin App):** Mahsulotlarni boshqarish, buyurtmalarni qayta ishlash hamda kirim/chiqim statistikasini kuzatish.

## 🛡 Xavfsizlik & Arxitektura
* **Ishonchli Autentifikatsiya:** Har bir so'rov server tomonida Telegram `initData` (HMAC-SHA256 signature) yordamida tekshiriladi.
* **Server-Side Hisob-Kitob:** Buyurtma summasi ma'lumotlar bazasidagi joriy narxlar asosida faqat serverda qayta hisoblanadi.
* **Rollar Nazorati:** Admin yo'llari faqat tegishli Telegram ID'ga ega tasdiqlangan foydalanuvchilar uchungina ochiq bo'ladi.

## 🛠 Texnologiyalar (Monorepo)
* **Frontend:** React, Telegram WebApp SDK, TailwindCSS, TypeScript.
* **Backend & Bot:** Python (`FastAPI` & `aiogram`) yoki Node.js frameworklari.
* **Workspace:** Frontend, Backend va Shared modullari birlashtirilgan NPM Workspace.
