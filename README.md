<div align="center">

# 🎯 Banner Grabber — أداة جلب معلومات الخدمات

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

أداة لجلب معلومات الخدمات والإصدارات من المنافذ المفتوحة على أي هدف، مكتوبة بلغة Python وتعمل على Termux و Kali Linux. تتصل بالخدمة مباشرة وتعرض الـ Banner الذي يكشف عن نوع الخدمة وإصدارها.

---

<div align="center" id="المميزات">

## ✨ المميزات

</div>

- 🎯 جلب Banner من 15 خدمة شائعة دفعة واحدة
- 🔍 فحص منفذ محدد بتفاصيل أكثر
- ⚡ تعدد الخيوط للسرعة القصوى
- 🏷️ كشف إصدارات الخوادم (Apache, Nginx, OpenSSH...)
- 📋 ملخص بالخدمات المكتشفة في النهاية
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
curl -o $PREFIX/bin/mud_bg.py https://raw.githubusercontent.com/mmuhacker/mud-bg/main/mud_bg.py
```

**الخطوة 5 — إعطاء صلاحية التشغيل**
```bash
chmod +x $PREFIX/bin/mud_bg.py
```

**الخطوة 6 — إنشاء رابط الاختصار**
```bash
ln -sf $PREFIX/bin/mud_bg.py $PREFIX/bin/bg
```

**⚡ أو قم بكل شيء بأمر واحد مجمّع**
```bash
pkg update && pkg upgrade -y && pkg install python tor curl fontconfig rust -y && pip install requests pysocks arabic-reshaper && pip install python-bidi==0.4.2 && curl -L "https://fonts.gstatic.com/s/notonaskharabic/v33/RrQ5bpV-9Dd1b1OAGA6M9PkyDuVBePeKNaxcsss0Y7bwvc-VaA.ttf" -o ~/.termux/font.ttf && termux-reload-settings && curl -o $PREFIX/bin/mud_bg.py https://raw.githubusercontent.com/mmuhacker/mud-bg/main/mud_bg.py && chmod +x $PREFIX/bin/mud_bg.py && ln -sf $PREFIX/bin/mud_bg.py $PREFIX/bin/bg && bg
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
sudo curl -o /usr/local/bin/mud_bg.py https://raw.githubusercontent.com/mmuhacker/mud-bg/main/mud_bg.py
```

**الخطوة 4 — إعطاء صلاحية التشغيل**
```bash
sudo chmod +x /usr/local/bin/mud_bg.py
```

**الخطوة 5 — إنشاء رابط الاختصار**
```bash
sudo ln -sf /usr/local/bin/mud_bg.py /usr/local/bin/bg
```

**⚡ أو قم بكل شيء بأمر واحد مجمّع**
```bash
sudo apt update && sudo apt upgrade -y && pip install requests arabic-reshaper python-bidi==0.4.2 --break-system-packages && sudo curl -o /usr/local/bin/mud_bg.py https://raw.githubusercontent.com/mmuhacker/mud-bg/main/mud_bg.py && sudo chmod +x /usr/local/bin/mud_bg.py && sudo ln -sf /usr/local/bin/mud_bg.py /usr/local/bin/bg && bg
```

---

<div align="center" id="التشغيل">

## 🚀 التشغيل

</div>

```bash
bg
```

**أو بالأمر الكامل**

```bash
mud_bg.py
```

---

<div align="center" id="طريقة-الاستخدام">

## 📖 طريقة الاستخدام


| الوضع | الوصف |
|-------|-------|
| `1` مسح كل الخدمات | فحص 15 خدمة شائعة دفعة واحدة |
| `2` منفذ محدد | فحص منفذ واحد بتفاصيل أكثر |

</div>
---

<div align="center" id="مثال">

## 💡 مثال

</div>

اختيارك: 1
أدخل الهدف: 192.168.1.1

  المنفذ  الخدمة        المعلومات
  ─────────────────────────────────
  [✓]  22      SSH           SSH-2.0-OpenSSH_8.9p1
  [✓]  80      HTTP          HTTP/1.1 200 OK | Server: Apache/2.4.54
  [✓]  3306    MySQL         5.7.39-MySQL Community Server

  [✓] الخدمات المكتشفة (3)


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

هذه الأداة مخصصة **لأغراض تعليمية واختبار الأنظمة التي تملك صلاحية اختبارها فقط**.
استخدامها على أنظمة بدون إذن يُعدّ مخالفاً للقانون.

---

<div align="center" id="المطوّر">

## 👨‍💻 المطوّر

**Muhannad Daher**

[![GitHub](https://img.shields.io/badge/GitHub-mmuhacker-black?style=for-the-badge&logo=github)](https://github.com/mmuhacker)

---

***Madarik Tools — صُنع بالعربية***

⭐ **إذا أعجبتك الأداة، لا تنسَ النجمة!** ⭐

</div>
