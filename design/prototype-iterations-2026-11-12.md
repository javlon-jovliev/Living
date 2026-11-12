# Prototip iteratsiyalari va qarorlar — 2026-11-12

**Status:** Suhbat yozuvi (Javlon ↔ Claude). `[Javlon]` — uning so‘zi yoki qarori; `[Claude]` — tahlil yoki taklif, qaror emas.  
**Prototiplar:** [prototypes/](../prototypes/README.md)

## 1. G‘oyaning mag‘zi o‘zgarmaydi

- `[Javlon]` Codex suhbatidan keyin g‘oya "inson niyatini hisoblashga yaqinlashtirish" tomon kengaygan edi. Javlon: **"g‘oyaning mag‘zi o‘zgarishini xohlamayman."**
- Mag‘iz (Javlonning ilgari aytgan talablari asosida):
  1. Har bir odamning o‘z doimiy raqamli makoni bor.
  2. Komponentlar hayotdagi kabi fizik qonunlarga bo‘ysunadi; odam ularni qo‘li bilan, editorsiz shakllantiradi.
  3. Shakl bilan birga funksiya ham o‘zgaradi; komponentlar birlashib yangi funksiya beradi, mantiqan mos kelmasa qo‘shilmaydi ("kimyo").
  4. Tayyor komponentlar, muhitlar va joylashuvlar bazasi; olish, o‘zgartirish, ulashish.
  5. O‘yin emas — kundalik ish uchun; ekran, klaviatura, tugma, scroll tushunchalarini tubdan o‘zgartiradi.
- `[Claude]` "Niyat" g‘oyasi *nima uchun* degan savolga javob; yuqoridagi besh band *qanday* degan savolga javob va Living'ni boshqa AI mahsulotlardan aynan shu ajratadi. VISION.md'dagi "niyat" bo‘limi mag‘izni siqib chiqarmasligi kerak.

## 2. Iteratsiyalar zanjiri

| Versiya | Javlonning talabi | Nima qilindi |
|---|---|---|
| v1 (2D) | "Qanday ishlashini tasavvur qilib olishim kerak" | Ishlaydigan 2D model: fizika, kimyo, ajratish, baza, orqaga |
| v2 (3D platforma) | Hammasi 3D; bir xil shakllar bo‘lmasin; tugma/oyna bo‘lmasin; ochilganda ma'lumot 3D joy egallasin; ochmasdan ichini tushunish | Har tur o‘z shaklida; ichidagi narsalar tashqaridan ko‘rinadi; bosganda ma'lumot havoga qatlam bo‘lib ko‘tariladi; hamma amal harakat bilan |
| v3 (qo‘l) | Barmoq harakati bilan boshqarish; hammasi bitta tarelkada bo‘lmasin; shakllar vazifaga mos va mantiqiy; ishoralarni bildiruvchi vaqtinchalik boshqaruv komponentlari | Kamera + MediaPipe; ochiq maydon; hayotiy shakllar (pachka, chek, kalendar, konvert, taxta); 8 ta ishora komponenti, tanilganda yonadi |
| v4 (halqa stol) | "O‘yin kabi statik makon bo‘ldi"; shaklni erkin boshqarish; markazda men, obyektlar atrofimda; bitta ish stoli; har tomondan ko‘rish, kattalashtirish, boshqa stolga o‘tish; obyekt ustida yozuv bo‘lmasin | Birinchi shaxs ko‘rinishi; halqa stol; chetidan tortib cho‘zish (kalendar → ko‘proq kun, ro‘yxat → bo‘sh qatorlar); 3 ta stol; yozuvsiz obyektlar; 10 ta ishora komponenti |

## 3. Boshqa qarorlar va fikrlar

- `[Javlon]` Fizik xususiyatlar real fizikaga yaqin bo‘lsin: rang, temperatura, impuls, 3D o‘lcham.
- `[Javlon]` Ishora komponentlari **vaqtinchalik**; har biri qaysi harakatni bildirishi ko‘rinib turishi kerak.
- `[Claude]` Modellarda ishlatilgan xususiyatlar lug‘ati (hypothesis): rang = tur; o‘lcham = ma'lumot miqdori; og‘irlik = summa (og‘irni surish qiyin); harorat = shoshilinchlik (issiq narsa ko‘tariladi); tortilish/itarilish = mos/mos emas.
- `[Claude]` Tez o‘tib ketishda tasodifiy birlashib ketmaslik uchun birlashish 0,2 soniya ustma-ust turishni talab qiladi.

## 4. Qo‘l bilan boshqarish: eng tez real yo‘l

- `[Claude]` Hozir: kompyuter kamerasi + Google MediaPipe Hand Landmarker (brauzerda, bepul). Cheklovlar: chuqurlik taxminiy; yorug‘lik va kadrdan chiqish kuzatuvni uzadi; havoda qo‘l uzoq ishlaganda charchaydi.
- `[Claude]` Keyingi daraja: Meta Quest 3/3S, WebXR Hand Input (har qo‘lga 25 bo‘g‘im). Avval kamerali variantda ishoralar tabiiyligini tekshirish arzonroq.

## 5. Hozirgi zaif joylar (v4)

- Shakl erkinligi faqat eni/bo‘yini tortish; egish, bukish, loy kabi ezish yo‘q.
- Ochilganda ichidagi ma'lumot hali matn.
- Haqiqiy kamera bilan sinalmagan.
- Obyektlar namunaviy; haqiqiy ma'lumotga ulanmagan.

## 6. Claude tavsiyasi: keyingi qadamlar (qaror emas)

1. Javlonning o‘zi v4'ni kamera bilan 15 daqiqa sinashi: qaysi ishora tabiiy, qaysi biri charchatdi yoki noto‘g‘ri tanildi.
2. Bitta haqiqiy kundalik ishni tanlash (masalan portfel va risk tahlili) va o‘sha ish uchun haqiqiy obyektlar; oddiy dastur bilan vaqtni solishtirish.
3. Mag‘izni kuchaytirish: loy kabi erkin shakllantirish va har bir shakl o‘zgarishi funksiyani o‘zgartirishi.
4. 3–5 kishi bilan tushuntirishsiz sinov: shakl o‘zi nimaligini ko‘rsatadimi?
5. G‘oya isbotlangach three.js / WebXR ga o‘tish.

Qilmaslik kerak: isbotlanmagan holda yangi effekt va obyektlar qo‘shishni davom ettirish.
