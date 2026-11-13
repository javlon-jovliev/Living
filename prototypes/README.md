# Prototiplar

**Status:** Ishlaydigan eskiz modellar (Claude, 2026-11-12). Mahsulot emas, g‘oyani qo‘lda his qilish uchun.  
**Ma'lumotlar:** hammasi namunaviy, hech narsa saqlanmaydi.  
**Tafsilotlar va qarorlar:** [Prototip iteratsiyalari](../design/prototype-iterations-2026-11-12.md)

## Qanday ochiladi

Faylni yuklab oling va brauzerda oching (Chrome tavsiya etiladi). Server kerak emas.  
Qo‘l ishoralari (v3, v4) uchun: kamerasi bor kompyuter, kameraga ruxsat va birinchi ochishda internet (qo‘l modeli Google MediaPipe'dan yuklanadi). Kamera bo‘lmasa, sichqoncha yoki barmoq bilan ishlaydi.

## Versiyalar

| Fayl | Nimani ko‘rsatadi | Javlonning fikri |
|---|---|---|
| [v1-2d-sandbox.html](v1-2d-sandbox.html) | 2D maydon. Fizika, "kimyo" (mos bo‘lsa birlashadi, bo‘lmasa itariladi), ajratish, tayyor baza, orqaga | Tasavvur uchun boshlang‘ich qadam |
| [v2-3d-platform.html](v2-3d-platform.html) | 3D platforma. Har tur o‘z shaklida, ichidagi narsa tashqaridan ko‘rinadi; tugma va oyna yo‘q, hammasi harakat bilan | "Hammasi bitta tarelkada yig‘ilmasin", "shakllar tasodifiy bo‘lmasin" |
| [v3-hand-gestures.html](v3-hand-gestures.html) | Kamera orqali qo‘l bilan boshqaruv (MediaPipe). Ochiq maydon, hayotiy shakllar, 8 ta vaqtinchalik ishora komponenti | "O‘yin kabi oldindan qurilgan statik makon", "obyekt ustida yozuv bo‘lmasin" |
| [v4-ring-desk.html](v4-ring-desk.html) | **Oxirgi versiya.** Foydalanuvchi markazda, ish stoli atrofni halqa bo‘lib o‘raydi; obyektni chetidan tortib shaklini o‘zgartirish; 3 ta ish stoli; yozuvsiz obyektlar; 10 ta ishora komponenti | Hali sinab ko‘rilmagan |

## v4 boshqaruvi

| Qo‘l ishorasi | Sichqoncha / sensor | Natija |
|---|---|---|
| O‘rtasidan qisish va siljitish | Obyektni o‘rtasidan sudrash | Olib yurish |
| Chetidan qisish va tortish | Obyekt chetidan sudrash | Shakli o‘zgaradi (kalendar: ko‘proq kun; ro‘yxat: bo‘sh qatorlar) |
| Tez qisib ochish | Bir marta bosish | Ichi ochiladi / yopiladi |
| Qisgancha silkitish | Sudragancha chapga-o‘ngga silkitish | Birlashgan obyekt ajraladi |
| Tez otib qo‘yib yuborish | Tez sudrab qo‘yib yuborish | Yo‘qotish |
| Musht | Bo‘sh joyni sudrash | Atrofga qarash |
| Ikki qo‘l bilan qisib cho‘zish | G‘ildirak / ikki barmoq | Oldinga-orqaga yurish |
| Kaftni yonga surish | ← / → | Boshqa ish stoliga o‘tish |
| Kaftni 1 soniya tutish | Ctrl+Z | Orqaga |
| Ikki kaft | Probel | Stol markaziga qaytish |

## Tekshiruv holati

- Sichqoncha bilan: brauzerda avtomatik sinovdan o‘tgan (birlashtirish, cho‘zish, ochish, ajratish, stol almashtirish); ~60 kadr/soniya.
- Qo‘l bilan: **faqat sun'iy qo‘l ma'lumotlari bilan** sinalgan. Haqiqiy kamera bilan sinalmagan (ish muhitida internet yopiq edi). Sezgirlik chegaralari real sinovdan keyin sozlanishi kerak.
- Telefon: sensor bilan ishlaydi; kamera yo‘q.

## Texnik eslatma

3D dvigatel kutubxonasiz, Canvas 2D ustida yozilgan (silindrik proyeksiya, painter's algorithm). Bu g‘oyani sinash uchun yetarli; g‘oya isbotlangach three.js / WebXR (Quest) ga o‘tish tavsiya etiladi.
