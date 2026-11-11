# Experiment 001 — yangi funksional obyektni bevosita yaratish

**Holat:** Proposed; hali o‘tkazilmagan.  
**Turi:** HCI + semantic composition proof-of-concept.  
**Etika:** haqiqiy maxfiy ma'lumotlarsiz, test datasida, ishtirokchi roziligi bilan.

## Tekshirilayotgan gipoteza

Foydalanuvchi editor va kod yozmasdan, oddiy bevosita harakatlar orqali ikki Living obyektidan **yangi ishlaydigan va qayta foydalaniladigan obyekt** hosil qila oladi.

Bu experiment faqat obyektlarni ko‘chirishni emas, **yangi behavior**ni tekshiradi.

## Minimal demo doirasi

4–6 ta Living-native obyekt; masalan:
- Expenses (transactions, amount, currency, date)
- Timeline (date range, filters)
- Tasks (status, due dates)
- Notes (text, references)
- Chart view
- Filter/aggregate transform

**Asosiy vazifa:** Expenses + Timeline → “Time-based spending” obyektiga aylantirish, filter qo‘shish, saqlash, yopib qayta ochish.

**Murakkab vazifa:** foydalanuvchi birinchi natijani yangi obyekt bilan ulab yanada foydali ko‘rinish yaratadi (masalan, Tasks + Timeline → risk/overdue view). Har bir kombinatsiya oldindan belgilangan capabilities doirasida bo‘ladi.

## Baseline

Shunga o‘xshash vazifani tayyor spreadsheet, dashboard yoki Notion'ga o‘xshash mavjud vositada bajarish. Muhim: baseline foydalanuvchilar uchun tanish va vazifaga mos bo‘lsin; ataylab yomon alternativ tanlamaslik kerak.

## Dizayn

**1-bosqich (qualitative, tavsiya):** 10–15 foydalanuvchi, ayniqsa dasturchi bo‘lmaganlar. Moderatsiyalangan usability session, think-aloud, muvaffaqiyatsiz tajribalarni ham qayd qilish.

**2-bosqich (comparative):** 30+ foydalanuvchidan boshlanadigan kontrbalanslangan sinov. Bu son **statistik quvvat kafolati emas**; sample size keyin effect size va power analysis asosida belgilanadi.

**3-bosqich (retention):** 7–14 kun foydalanuvchining o‘zi yaratgan obyektga qaytishi va uni qayta ishlatishi kuzatiladi.

## O‘lchovlar

| Metric | Izoh |
|---|---|
| Task completion | To‘g‘ri natija hosil bo‘ldimi? |
| Time to useful object | Birinchi foydali behaviorli obyektgacha vaqt |
| Semantic correctness | Natija data va units bilan haqiqatan to‘g‘rimi? |
| Recovery time | Xatoni mustaqil orqaga qaytarish |
| Accidental edits | Gestures noto‘g‘ri tushunilgan holatlar |
| Cognitive load | Foydalanuvchi e'lon qilgan qiyinchilik, qisqa anketalar |
| Repeat use | Keyingi kun/haftada obyekt yana ishlatildimi? |
| Baseline comparison | Shu vazifa bo‘yicha mavjud vositalarga nisbatan yaxshimi? |

## Oldindan belgilanishi mumkin bo‘lgan mezonlar (proposal)

- Ishtirokchilarning aksariyati yangi obyektga birinchi urinishda yoki qisqa o‘rganishdan keyin mustaqil yeta olsin.
- Muhim ruxsatsiz tashqi amal va ma'lumot yo‘qotish: **0** (safety gate).
- Foydalanuvchi qayta kirganida o‘z obyekti va uning behavior'i saqlangan bo‘lsin.
- Baseline bilan solishtirganda maqsadli vazifa uchun real foyda yoki oddiy vositada yo‘q yangi imkoniyat ko‘rinsin.
- Muammolar va ularning takrorlanishi yozib borilsin.

Aniq sonli thresholdlar tadqiqot boshlanishidan oldin, pilot natijalari va real vazifa murakkabligiga qarab rasmiylashtiriladi. Mezonni natijani ko‘rgandan keyin o‘zgartirish noto‘g‘ri xulosaga olib keladi.

## Qanday holatda gipoteza zaiflashadi?

- Kompozitsiya muntazam izohli AI chatga bog‘lanib qolsa;
- Foydalanuvchilar tashqi yordam bilan ham niyatini ifodalay olmasa;
- Hosil bo‘lgan obyekt noto‘g‘ri ma'lumot bilan ishonchli ko‘rinsa;
- Eski vosita ancha tez va ishonchli bo‘lsa;
- Yaratilgan obyekt bir martalik demo bo‘lib, keyin ishlatilmasa.

## Natijalarni saqlash shakli

Natija o‘tkazilganidan keyin alohida fayl ochiladi:
- Date; protocol version; sample/recruitment;
- Tasks, baseline, raw metric summary;
- Confirmed findings / contradictory evidence;
- Limitations; next action; explicit go/no-go.

**Bog‘liq:** [Living Object Model](../concepts/living-object-model.md) · [Risks](../risks/risk-register.md) · [Open Questions](../open-questions.md)
