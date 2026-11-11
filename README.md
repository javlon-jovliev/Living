# Living

> **Living** is a research initiative exploring *malleable computing*: a personal digital environment that people can reshape, compose, and extend directly — like working with physical material.

**Repository:** Research & Knowledge Base (not application source code)  
**State:** Early research, November 2026  
**Language:** Asosan o‘zbekcha; texnik terminlar inglizcha saqlanishi mumkin.

## Living nima?

Living oddiy UI builder, sayt quruvchisi yoki faqat rang/joylashuvni sozlash imkoniyati emas. U har bir foydalanuvchining **personal digital space** muhitida obyektlarning ko‘rinishi, ma'lumotlari va xatti-harakatlarini **ish jarayonining o‘zida**, alohida editor ochmasdan shakllantira olishini o‘rganadi.

Ideal holatda ikki obyekt birlashib, oldin mavjud bo‘lmagan yangi foydali funksional obyektga aylanishi mumkin. Biroq **har qanday kombinatsiya foydali va to‘g‘ri natija berishi** hozircha isbotlanmagan.

Uzoq muddatli yo‘nalish — OS darajasidagi personal computing environment; dastlabki tekshiruv uchun yangi kernel majburiy emas.

## Boshlash uchun: hujjatlar xaritasi

| Yo‘nalish | Hujjat | Status |
|---|---|---|
| G‘oya va prinsiplar | [VISION.md](VISION.md) | Vision / intent |
| Asosiy atamalar | [GLOSSARY.md](GLOSSARY.md) | Working definitions |
| Keng baholash | [Feasibility assessment](research/feasibility-2026-11-11.md) | Research synthesis / assessment |
| Oldingi ishlar | [Prior art](research/prior-art.md) | Evidence + interpretation |
| Ilmiy / rasmiy manbalar | [Sources register](research/sources.md) | Curated sources, verification status |
| Kimga foydali va bozor | [Product value](research/product-value.md) | Hypotheses |
| Asosiy hisoblash modeli | [Living Object Model](concepts/living-object-model.md) | Technical proposal |
| Editor'siz shakllantirish | [Direct manipulation](concepts/direct-manipulation.md) | Interaction proposal |
| Fizika va "kimyo" qoidali muhit | [Fizik muhit](concepts/physical-environment.md) | Vision + tahlil |
| Qo‘l nimani ifodalay oladi | [Fizik harakat chegaralari](concepts/physical-actions-limits.md) | Tahlil / hypothesis |
| 2025–2026 mahsulotlar va tadqiqotlar | [Market evidence](research/market-evidence-2026-11.md) | Evidence + talqin |
| Mustaqil tanqidiy baho | [Critical review](research/critical-review-2026-11-11.md) | Fikr; qaror emas |
| Xavflar | [Risk register](risks/risk-register.md) | Initial risk assessment |
| Birinchi sinov | [Experiment 001](experiments/001-object-composition.md) | Proposed; not performed |
| Hal qilinmagan savollar | [Open questions](open-questions.md) | Research backlog |
| Rivojlanish bosqichlari | [Roadmap](proposals/roadmap.md) | Proposal; not decided |

## Nimalar ma'lum, nimalar noma'lum?

**Mavjud texnologiyalar bilan real:** erkin canvas, grafik obyektlar, persisted state, type-checked components, granular permissions, local-first patterns.

**Loyihada tekshirilishi kerak:** oddiy foydalanuvchi uchun tabiiy gesture grammar, semantik kompozitsiya, yangi behavior'ning tushunarliligi, real task benefit, retention.

**Hozircha va'da qilinmaydi:** universal semantik kompozitsiya yoki yopiq uchinchi tomon ilovalari ichki qismlarini mutlaq erkin o‘zgartirish.

## Bilimlar bilan ishlash qoidasi

Har bir yangi hujjat imkon qadar quyidagilarni aniq ajratsin:

- **Evidence:** manba; nimalar amalda isbotlangan; sample size va cheklovlar.
- **Hypothesis:** hali sinalmagan, rad qilinishi mumkin bo‘lgan faraz.
- **Proposal:** texnik, UX yoki mahsulot yo‘li; hali qabul qilingan qaror emas.
- **Experiment:** usul, oldindan qo‘yilgan mezon, natija, cheklov.
- **Decision:** muqobil variantlar ko‘rilgan va sabab bilan qabul qilingan tanlov (qaror qilinmaguncha “decision” deb yozilmaydi).

Manbalarni [research/sources.md](research/sources.md) reyestrida saqlang. Ikkilamchi xulosani manba dalili sifatida ko‘rsatmang. Salbiy natijalarni ham yozing.

## Keyingi eng muhim bosqich

[Experiment 001](experiments/001-object-composition.md) bilan aniqlash: foydalanuvchi ikkita Living-native obyektni editor/kodsiz birlashtirib, **yangi ishlaydigan va saqlanadigan** obyekt hosil qila oladimi? Bu ish real vazifada mavjud vositadan yaxshiroqmi?

Yuqoridagi protokol **hozircha taklif**; eksperiment bajarilgan emas.

## Ochiqlik, mualliflik va xavfsizlik

Bu public repository. Unda shaxsiy yoki maxfiy ma'lumot, token, kalit va nashr qilinishi rejalashtirilmagan materiallarni saqlamang. Tashqi maqolalarning to‘liq matnini litsenziyasiz ko‘chirmang; havola va o‘z tahlilingizni yozing. Kontent litsenziyasi alohida tanlanmaguncha ochiq ko‘rinish avtomatik ravishda qayta ishlatish huquqi bermaydi.

---

*Living is currently a research direction, not a shipped operating system. The repository is expected to change as evidence accumulates.*
