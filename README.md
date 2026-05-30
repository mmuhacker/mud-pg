<div align="center">

# 🔐 Password Generator — أداة توليد كلمات المرور

**تعمل على نظام Kali Linux و تطبيق Termux**

꧁ঔৣ☬ Muhannad Daher ☬ঔৣ꧂

---

![Version](https://img.shields.io/badge/Version-1.0-blue?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Kali_Linux-green?style=for-the-badge&logo=kalilinux)
![Platform](https://img.shields.io/badge/Platform-Android-green?style=for-the-badge&logo=android)
![Python](https://img.shields.io/badge/Python-3.x-yellow?style=for-the-badge&logo=python)
![License](https://img.shields.io/badge/License-MIT_License-red?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge)

---

**المحتويات:**

</div>

- [الوصف](#الوصف)
- [المميزات](#المميزات)
- [التثبيت على Termux](#التثبيت-على-termux)
- [التثبيت على Kali Linux](#التثبيت-على-kali-linux)
- [التشغيل](#التشغيل)
- [طريقة الاستخدام](#طريقة-الاستخدام)
- [مثال](#مثال)
- [المتطلبات](#المتطلبات)
- [إخلاء المسؤولية](#إخلاء-المسؤولية)
- [المطوّر](#المطوّر)

---

<div align="center" id="الوصف">

## 📌 الوصف

</div>

أداة لتوليد كلمات مرور قوية وآمنة، مكتوبة بلغة Python وتعمل على Termux و Kali Linux. تعتمد على مكتبة `secrets` المدمجة في Python للحصول على عشوائية حقيقية من نظام التشغيل، مع تقييم تلقائي لقوة كل كلمة مرور.

---

<div align="center" id="المميزات">

## ✨ المميزات

</div>

- 🎲 عشوائية حقيقية باستخدام مكتبة `secrets`
- 🔑 توليد كلمة مرور واحدة بمعايير مخصصة بالكامل
- 📝 توليد عبارة مرور (passphrase) سهلة التذكر
- 📦 توليد مجموعة كلمات مرور دفعة واحدة
- 📊 تقييم تلقائي للقوة (ضعيفة / متوسطة / قوية / قوية جداً)
- 💾 حفظ كلمات المرور في ملف نصي
- 🌍 واجهة عربية بالكامل

---

<div align="center" id="التثبيت-على-termux">

## ⚙️ التثبيت

### Termux

</div>

**الخطوة 1 — تحديث النظام**
```bash
pkg update && pkg upgrade -y
```

**الخطوة 2 — تثبيت المتطلبات** *(لمرة واحدة فقط)*
```bash
pkg install python tor curl fontconfig rust -y
```
```bash
pip install requests pysocks arabic-reshaper
pip install python-bidi==0.4.2
```

**الخطوة 3 — تثبيت الخط العربي** *(لمرة واحدة فقط)*
```bash
curl -L "https://fonts.gstatic.com/s/notonaskharabic/v33/RrQ5bpV-9Dd1b1OAGA6M9PkyDuVBePeKNaxcsss0Y7bwvc-VaA.ttf" -o ~/.termux/font.ttf
termux-reload-settings
```

**الخطوة 4 — تنزيل الأداة**
```bash
curl -o $PREFIX/bin/mud_pg.py https://raw.githubusercontent.com/mmuhacker/mud-pg/main/mud_pg.py
```

**الخطوة 5 — إعطاء صلاحية التشغيل**
```bash
chmod +x $PREFIX/bin/mud_pg.py
```

**الخطوة 6 — إنشاء رابط الاختصار**
```bash
ln -sf $PREFIX/bin/mud_pg.py $PREFIX/bin/pg
```

**⚡ أو قم بكل شيء بأمر واحد مجمّع**
```bash
pkg update && pkg upgrade -y && pkg install python tor curl fontconfig rust -y && pip install requests pysocks arabic-reshaper && pip install python-bidi==0.4.2 && curl -L "https://fonts.gstatic.com/s/notonaskharabic/v33/RrQ5bpV-9Dd1b1OAGA6M9PkyDuVBePeKNaxcsss0Y7bwvc-VaA.ttf" -o ~/.termux/font.ttf && termux-reload-settings && curl -o $PREFIX/bin/mud_pg.py https://raw.githubusercontent.com/mmuhacker/mud-pg/main/mud_pg.py && chmod +x $PREFIX/bin/mud_pg.py && ln -sf $PREFIX/bin/mud_pg.py $PREFIX/bin/pg && pg
```

---

<div align="center" id="التثبيت-على-kali-linux">

### Kali Linux

</div>

**الخطوة 1 — تحديث النظام**
```bash
sudo apt update && sudo apt upgrade -y
```

**الخطوة 2 — تثبيت المتطلبات** *(لمرة واحدة فقط)*
```bash
pip install requests arabic-reshaper python-bidi==0.4.2 --break-system-packages
```

**الخطوة 3 — تنزيل الأداة**
```bash
sudo curl -o /usr/local/bin/mud_pg.py https://raw.githubusercontent.com/mmuhacker/mud-pg/main/mud_pg.py
```

**الخطوة 4 — إعطاء صلاحية التشغيل**
```bash
sudo chmod +x /usr/local/bin/mud_pg.py
```

**الخطوة 5 — إنشاء رابط الاختصار**
```bash
sudo ln -sf /usr/local/bin/mud_pg.py /usr/local/bin/pg
```

**⚡ أو قم بكل شيء بأمر واحد مجمّع**
```bash
sudo apt update && sudo apt upgrade -y && pip install requests arabic-reshaper python-bidi==0.4.2 --break-system-packages && sudo curl -o /usr/local/bin/mud_pg.py https://raw.githubusercontent.com/mmuhacker/mud-pg/main/mud_pg.py && sudo chmod +x /usr/local/bin/mud_pg.py && sudo ln -sf /usr/local/bin/mud_pg.py /usr/local/bin/pg && pg
```

---

<div align="center" id="التشغيل">

## 🚀 التشغيل

</div>

```bash
pg
```

**أو بالأمر الكامل**

```bash
mud_pg.py
```

---

<div align="center" id="طريقة-الاستخدام">

## 📖 طريقة الاستخدام


1. اختر نوع التوليد:

| الوضع | الوصف |
|-------|-------|
| `1` كلمة مرور | تحكم كامل بالطول والمعايير 🔑 |
| `2` عبارة مرور | passphrase سهلة التذكر 📝 |
| `3` مجموعة | عدة كلمات دفعة واحدة مع حفظ خياري 📦 |

</div>

2. في وضع كلمة المرور تختار:
   - الطول (الافتراضي 16)
   - أحرف كبيرة A-Z
   - أحرف صغيرة a-z
   - أرقام 0-9
   - رموز خاصة

---

<div align="center" id="مثال">

## 💡 مثال

</div>

اختيارك: 1
الطول: 16

  X7#mK9qL@nR2wP5v   [قوية جداً ✓]
  الطول: 16 حرف

اختيارك: 2
عدد الكلمات: 4

  rapid-forge-nexus-ghost-3847   [قوية]
  الطول: 29 حرف


---

<div align="center" id="المتطلبات">

## 🔧 المتطلبات


| المتطلب | الوصف |
|---------|-------|
| Python 3.6+ | لغة البرمجة |
| arabic-reshaper | دعم النص العربي |
| python-bidi | اتجاه النص العربي |
| curl | تنزيل الأداة |

</div>

> ⚠️ **ملاحظة:** بدون تثبيت `arabic-reshaper` و `python-bidi` سيظهر النص العربي معكوساً ومتقطعاً.

---

<div align="center" id="إخلاء-المسؤولية">

## ⚖️ إخلاء المسؤولية

</div>

هذه الأداة مخصصة **لأغراض تعليمية فقط**.
لا تستخدمها لأغراض غير مشروعة.

---

<div align="center" id="المطوّر">

## 👨‍💻 المطوّر

**Muhannad Daher**

[![GitHub](https://img.shields.io/badge/GitHub-mmuhacker-black?style=for-the-badge&logo=github)](https://github.com/mmuhacker)

---

***Madarik Tools — صُنع بالعربية***

⭐ **إذا أعجبتك الأداة، لا تنسَ النجمة!** ⭐

</div>
