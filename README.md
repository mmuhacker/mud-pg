# 🔐 Password Generator — أداة توليد كلمات المرور
**المطور:** ꧁ঔৣ☬ Muhannad Daher ☬ঔৣ꧂ | **الإصدار:** 1.0 | **المستودع:** `mud-pg`

---

## 📌 الوصف
أداة لتوليد كلمات مرور قوية وآمنة، مكتوبة بلغة Python وتعمل على Termux و Kali Linux. تعتمد على مكتبة `secrets` المدمجة في Python للحصول على عشوائية حقيقية من نظام التشغيل، مع تقييم تلقائي لقوة كل كلمة مرور.

---

## ✨ المميزات
- 🎲 عشوائية حقيقية باستخدام مكتبة `secrets`
- 🔑 توليد كلمة مرور واحدة بمعايير مخصصة بالكامل
- 📝 توليد عبارة مرور (passphrase) سهلة التذكر
- 📦 توليد مجموعة كلمات مرور دفعة واحدة
- 📊 تقييم تلقائي للقوة (ضعيفة / متوسطة / قوية / قوية جداً)
- 💾 حفظ كلمات المرور في ملف نصي
- 🌍 واجهة عربية بالكامل

---

## ⚙️ التثبيت

### Termux
```bash
curl -o $PREFIX/bin/mud_pg.py https://raw.githubusercontent.com/mmuhacker/mud-pg/main/mud_pg.py
chmod +x $PREFIX/bin/mud_pg.py
ln -sf $PREFIX/bin/mud_pg.py $PREFIX/bin/pg
```

### Kali Linux
```bash
sudo curl -o /usr/local/bin/mud_pg.py https://raw.githubusercontent.com/mmuhacker/mud-pg/main/mud_pg.py
sudo chmod +x /usr/local/bin/mud_pg.py
sudo ln -sf /usr/local/bin/mud_pg.py /usr/local/bin/pg
```

---

## 🚀 التشغيل
```bash
pg
# أو
mud_pg.py
```

---

## 📖 طريقة الاستخدام

```
1. اختر نوع التوليد:
   [1] كلمة مرور  — تحكم كامل بالطول والمعايير  🔑
   [2] عبارة مرور — passphrase سهلة التذكر       📝
   [3] مجموعة     — عدة كلمات دفعة مع حفظ خياري  📦

2. في وضع كلمة المرور تختار:
   — الطول (الافتراضي 16)
   — أحرف كبيرة A-Z
   — أحرف صغيرة a-z
   — أرقام 0-9
   — رموز خاصة
```

---

## 💡 أمثلة على المخرجات

**كلمة مرور (16 حرف):**
```
  X7#mK9qL@nR2wP5v   [قوية جداً ✓]
  الطول: 16 حرف
```

**عبارة مرور:**
```
  rapid-forge-nexus-ghost-3847   [قوية]
  الطول: 29 حرف
```

**مجموعة كلمات مرور:**
```
   1.  Kw#9mXqL@nR2wP5v   [قوية جداً ✓]
   2.  Bz$7tYpM!kS4vN8j   [قوية جداً ✓]
   3.  Qr@5nHwK#mL8vX2p   [قوية جداً ✓]
```

---

## 🔧 المتطلبات
- Python 3.6 أو أحدث
- لا توجد مكتبات خارجية

```bash
# التثبيت على Termux إذا لم يكن Python موجوداً
pkg install python
```

---

## ⚖️ إخلاء المسؤولية
هذه الأداة مخصصة **لأغراض تعليمية فقط**.
لا تستخدمها لأغراض غير مشروعة.

---

*🇯🇴 Madarik Tools — صُنع بالعربية*
