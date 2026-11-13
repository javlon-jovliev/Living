# Fizik muhit: komponentlar fizika va "kimyo" qoidalariga bo‘ysunadi

**Status:** Vision (Javlon) + dastlabki tahlil (Claude). Sinovdan o‘tmagan.  
**Sana:** 2026-11-11

## G‘oya (Javlon)

- Muhitdagi komponentlar hayotdagi kabi **fizik qonunlarga bo‘ysunadi**.
- Foydalanuvchi ular bilan erkin amallar bajaradi: ushlaydi, itaradi, birlashtiradi, ajratadi.
- Maqsad: inson va hisoblash mashinasini yanada uyg‘unlashtirish; klaviatura, ekran, ilova, tugma, scroll tushunchalarini tubdan o‘zgartirish.
- **Kimyo qoidasi:** ikki komponentni qo‘shish mantiqan ma'nosiz bo‘lsa, ular qo‘shilmaydi — xuddi aralashmaydigan moddalar kabi.
- Rang, temperatura, impuls, 3D o‘lcham kabi tushunchalar muhitning bir qismi bo‘ladi.
- **Baza:** tayyor komponentlar, muhitlar va joylashuvlar. Foydalanuvchi ularni oladi, ishlatadi, o‘zgartiradi. O‘zi yasaganini xohlasa boshqalarga ulashadi.
- **Bu o‘yin maydoni emas.** Maqsad — haqiqiy odamlar kundalik ishida ishlatadigan qulay innovatsiya.

## Nima uchun bu oldingi tasvirdan kuchliroq (tahlil)

| Jihat | Izoh |
|---|---|
| Kimyo qoidasi | "Ikki obyekt qo‘shilsa nima chiqadi?" degan asosiy muammoga javob beradi: mos kelmasa, qo‘shilmaydi. Har bir komponentda "valentlik" bor — nima qabul qiladi, nima beradi. Mos bo‘lsa tortiladi, bo‘lmasa itariladi. Foydalanuvchi qoidani o‘qimaydi, ko‘radi. |
| Tayyor baza va ulashish | Dalillar ko‘pchilik o‘zi yasashni xohlamasligini ko‘rsatadi ([market evidence](../research/market-evidence-2026-11.md)). Baza bo‘lsa ko‘pchilik tayyorini oladi, ozchilik yasaydi. |

Texnik jihatdan "valentlik" — bu [Living Object Model](living-object-model.md)dagi typed capabilities'ning ko‘zga ko‘rinadigan shakli.

## Hal qilinishi kerak bo‘lgan muammolar

1. **Fizik xususiyatlarning ma'nosi.** Haqiqiy fizikani tushunamiz, chunki unda yashaymiz. "Faylning temperaturasi" esa o‘ylab topilgan ma'no; uni yodlash kerak bo‘lsa, bu yangi til bo‘lib qoladi. Kichik va o‘zgarmas lug‘at kerak.
2. **Klaviaturani butunlay yo‘qotib bo‘lmaydi.** Batafsil: [Fizik harakat chegaralari](physical-actions-limits.md).
3. **3D oddiy ekranda yomonroq ishlaydi.** Obyektlar bir-birini to‘sadi, chuqurlik sezilmaydi. Haqiqiy 3D uchun VR/AR kerak; uning foydalanuvchisi kam.
4. **Valentlikni kimdir belgilaydi.** Har bir yangi komponent uchun yasagan odam yoki AI. Xato belgilansa butun "kimyo" buziladi.

## Xususiyatlar lug‘ati — taklif (hypothesis)

| Fizik xususiyat | Mumkin bo‘lgan ma'no |
|---|---|
| O‘lcham | Ma'lumot miqdori |
| Temperatura | Qanchalik tez-tez o‘zgaryapti / muddat qanchalik yaqin |
| Og‘irlik | Muhimlik |
| Rang | Tur (xat, vazifa, pul, sana...) |
| Tortilish / itarilish | Mos kelish / kelmaslik |

Bu ro‘yxat taklif. Qaysi moslik odamlarga tabiiy tuyulishini faqat sinov ko‘rsatadi. Muhim shart: har bir xususiyat **hamma joyda bir xil ma'noni** bildirsin.

## Kundalik ishda foydalanish shartlari

Odam yangi vositaga uch shart bilan o‘tadi:

1. Hozirgi usuldan **tezroq** bo‘lsa (chiroyli yoki qiziq bo‘lishi yetmaydi).
2. **Besh daqiqada** o‘rgansa.
3. O‘zining **haqiqiy ma'lumoti** ichida bo‘lsa: pochta, fayllar, kalendar, pul. Bo‘sh muhitga hech kim qaytmaydi.

Uchinchi shart eng qiyini: muhitni yasash oson, uni odamning mavjud ma'lumotiga ulash qiyin.

## Bir kunlik misol (illyustratsiya, isbot emas)

Ertalab muhit ochiladi. Bugungi xatlar, vazifalar, uchrashuvlar obyekt bo‘lib turibdi. Muddati yaqinlari issiq va oldinda. Xatni vazifalar tomon itarsangiz, u vazifaga aylanadi. Xatni xarajatlar jadvaliga yaqinlashtirsangiz, itariladi — mos emas. Hisob-fakturani yaqinlashtirsangiz, yopishadi va summa qo‘shiladi.

Har bir harakat hozirgi 3–4 bosishdan tezroq bo‘lishi shart; aks holda odam eski usulga qaytadi.

## Birinchi sinov uchun minimal doira (proposal)

- 2D maydon (3D emas);
- 5–6 komponent;
- 3 ta fizik xususiyat, har biri aniq ma'no bilan;
- bitta kimyo qoidasi: tortiladi yoki itariladi;
- bitta kasb va uning har kuni takrorlanadigan bitta ishi.

## Ochiq savollar

- Birinchi foydalanuvchi kim va qaysi kundalik ish?
- Oddiy ekranmi yoki VR/AR?
- Qaysi fizik xususiyat qaysi ma'noga tabiiy mos keladi?

To‘liq ro‘yxat: [Open questions](../open-questions.md).
