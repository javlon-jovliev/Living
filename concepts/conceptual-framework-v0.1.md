# Living — Conceptual Framework v0.1

**Holat:** Draft / konseptual taklif. Ishlaydigan tizim yoki tasdiqlangan mahsulot spetsifikatsiyasi emas.  
**Sana:** 2026-11-12  
**Asos:** loyiha asoschisi bilan suhbatdagi maqsadlar va oldingi Living tadqiqotlari.

## 1. Living'ning maqsadi (Purpose)

**Living — insonning fikrlashi, niyati va kreativligini hisoblash mashinalari bilan chuqurroq integratsiya qilishga intiladigan hisoblash muhiti konsepsiyasi.**

Asosiy maqsad: biror narsani yaratish yoki kompyuter bilan ishlash uchun kerak bo‘ladigan **texnik va kognitiv vositachilik xarajatlarini kamaytirish**, odamning tasavvurini sinovdan o‘tkaziladigan, tushuniladigan va foydali hisoblash natijalariga yaqinlashtirish.

Living:
- o‘yin, Minecraft-ga o‘xshash qurilish maydonchasi yoki bezakli desktop emas;
- faqat yangi UI, AI chat, vizual app builder yoki fayllar menyusi emas;
- faqat mutaxassislar uchun emas; ammo turli domenlarda tekshiruv va javobgarlik zarur;
- uzoq muddatda ekran/sichqoncha/klaviatura bilan bog‘liq an'anaviy paradigma va hatto apparat shakllarini qayta ko‘rib chiqishga intiladi;
- hozircha yangi hardware yoki OS yadrosi haqidagi **qarorni** talab qilmaydi.

### North-star question

> Inson o‘z fikri va niyatini minimal texnik to‘siq bilan qanday qilib xavfsiz, tushunarli, qayta ishlanadigan hisoblash jarayoniga aylantira oladi?

### North-star outcome

Foydalanuvchi mavjud vositalar bilan murakkab, uzoq yoki qiyin bo‘lgan vazifani Living yordamida **muvaffaqiyatli**, **tushunib**, **ishonchliroq yoki osonroq** bajara oladi. Vizual joziba yetarli mezon emas.

## 2. Mantiqiy qatlamlar: maqsad → paradigma → model → interaksiya → texnologiya

| Layer | Savol | Mazmun | Nima bilan adashtirmaslik kerak? |
|---|---|---|---|
| **Purpose** | Nima uchun? | Inson kreativligi, agency va unumdorligini kuchaytirish | OS, 3D, AI, yangi qurilma |
| **Paradigm** | Inson–mashina munosabati qanday? | Intent-driven, malleable, continuous co-creation | Universal bir xil UI |
| **Computational model** | Hisoblash nimalardan iborat? | Objects, capabilities, relations, transformations, context | Faqat shakl yoki canvas |
| **Interaction model** | Inson qanday ishlaydi? | Bevosita manipulyatsiya + til + gesture + boshqa modality | Faqat sichqoncha yoki VR |
| **Implementation** | Qanday quriladi? | Runtime, renderer, AI, permissions, storage, OS adapter, hardware | Maqsadning o‘zi |

**Qoida:** Pastki qatlamlardagi texnik tanlovlar yuqoridagi maqsadga xizmat qiladi, aksincha emas.

## 3. Asosiy tushunchalar (working definitions)

- **Human:** maqsad, qadriyat va ijodiy yo‘nalish egasi. Qarorlar ustidan nazorat saqlanadi.
- **Intent:** foydalanuvchi xohlagan natija; ko‘pincha noaniq yoki qisman ifodalangan.
- **Context:** vazifa, vaziyat, mavjud data, tarix, cheklovlar, xavfsizlik/ruxsatlar.
- **Space:** vaqt davomida saqlanadigan, foydalanuvchi shakllantiradigan hisoblash muhiti.
- **Object:** identifikatori, ko‘rinishi, data, state, behavior, capability, permissions, history mavjud bo‘lgan hisoblash birligi (taklif).
- **Capability:** obyekt aniq qanday amallarni taklif qiladi yoki qanday resurslarga kira oladi.
- **Relation:** obyektlar orasidagi ma'lumot, bog‘liqlik, ma'no yoki bajarilish munosabati.
- **Transformation:** obyekt, bog‘lanish yoki behaviorning aniq o‘zgarishi.
- **Feedback:** tizimning natijani ko‘rsatishi; foydalanuvchi aniqlashtirishi va qayta ishlashi.

### Living Object — dastlabki mantiqiy model

`O = (Identity, Data, State, View, Behavior, Capabilities, Permissions, History)`.

Bu **yangi algoritm isboti emas**, terminlar orasidagi munosabatni aniqlovchi ishchi model. Shape/View o‘zgarsa, Identity/Data/Behavior avtomatik yo‘qolmasligi kerak. Batafsil: [Living Object Model](living-object-model.md).

## 4. Human–Computer Creative Loop

```text
Human intent / imagination
          ↓
Context + interpretation
          ↓
Candidate computational model
          ↓
Preview + verification + permission
          ↓
Execution / observable result
          ↓
Human feedback and refinement
          ↺
```

- **Interpretation** niyatni tushunishga urinadi, lekin noaniqlikni yashirmaydi.
- **Candidate model** yangi obyekt, transformatsiya, workflow yoki mavjud obyektning yaxshilangan ko‘rinishi bo‘lishi mumkin.
- **Verification** tur, ma'lumot birliklari, ruxsat, hisoblash correctness va kutilgan natijani tekshiradi.
- **Execution** xavfsiz runtime ichida yuz beradi; tashqi qaytarib bo‘lmaydigan harakat alohida ehtiyot choralarini talab qiladi.
- **Feedback** ijodiy jarayonning bir qismi; AI foydalanuvchining o‘rniga yakuniy maqsadni belgilamaydi.

**Muhim farq:** bu “prompt → kod → tayyor dastur” degan chiziqli jarayon emas. Inson va hisoblash muhiti iterativ ravishda birga shakllanadi.

## 5. Minimal computational operations — proposal

| Amal | Mazmun |
|---|---|
| Create | Yangi obyekt yoki hisoblash imkoniyati yaratish |
| Manipulate | Shape, data, state yoki parametrni o‘zgartirish |
| Connect | Obyektlar orasida aloqani belgilash |
| Compose | Ikki yoki undan ortiq capabilitydan yangi behavior yaratish |
| Separate | Aloqa yoki kompozitsiyani ajratish |
| Inspect | Amalning nima va nima uchun bo‘layotganini ko‘rish |
| Simulate | Bajarishdan oldin taxminiy natijani tekshirish |
| Restore | Holat yoki o‘zgarishni qaytarish |

Bu **backend semantik amallari**, majburiy tugmalar paneli emas. Bir amal qo‘l, ovoz, yozuv yoki boshqa modality bilan ifodalanishi mumkin.

## 6. Semantic composition

Konseptual ifoda:

`Compose(O1, O2, Goal, Context) -> Candidates | NeedClarification | Incompatible`

Hamma kombinatsiya uchun bitta ma'noli natija **kafolatlanmaydi**. Uchta tekshiruv kerak:

1. **Structural / typed compatibility:** interfeyslar, birliklar, input/output.
2. **Semantic / intentional fitness:** natija foydalanuvchi maqsadiga mos keladimi?
3. **Safety and permission:** ishga tushirish mumkinmi va qanday chegarada?

Masalan `Expenses + Timeline` → vaqt bo‘yicha xarajatlar tahlili bo‘lishi mumkin. `Email + Expenses` kontekstdan kelib chiqib invoice parsing bo‘lishi yoki umuman mos kelmasligi mumkin.

**Physical chemistry** (moslikni tortilish/ulanish orqali ifodalash) — shu modelning **mumkin bo‘lgan interaksiya metaforasi**, butun paradigma emas.

## 7. Universal deganda nima nazarda tutiladi?

Living har bir soha uchun bir xil ekran, bir xil 3D dunyo yoki bir xil gesture to‘plami bo‘lishini talab qilmaydi.

**Universal prinsiplar**, **domen-spetsifik obyektlar va ko‘rinishlar**:
- Tadqiqot: manba, ma'lumot, gipoteza, tahlil.
- Muhandislik: parametr, cheklov, simulyatsiya.
- Biznes: resurs, jarayon, vaqt, qaror.
- Kreativ ish: tovush, tasvir, shakl, harakat.

Domen bo‘yicha foyda hali tajribada o‘lchanmagan. Mavjud matn, jadval, klaviatura va kod ayrim vazifalarda eng yaxshi usul bo‘lishi mumkin.

## 8. Mustahkam prinsiplar

1. Inson agency'si va tushunarlilik.
2. Foydali natija vizual yangilikdan ustun.
3. O‘zgartirish ish jarayonining ichida; majburiy alohida editor emas.
4. Noaniq niyatni yashirin taxmin bilan yakunlamaslik.
5. Muhim amallarda preview, trace, permissions va rollback.
6. Device/modality mustaqil mantiqiy yadro.
7. Accessibility va progressive complexity.
8. AI va deterministik mexanizmlar vazifaga qarab hamkorlik qiladi.
9. Tayyor komponentlar bilan ishni boshlash mumkin; noldan qurish majburiy emas.

## 9. Noma'lum va ehtiyotli baholar

- Istalgan ikki obyektning semantik birlashishi hal etilmagan.
- Kod yozmaslik foydalanuvchining domen bo‘yicha javobgarligini yo‘qotmaydi.
- Inson niyatini avtomatik aniqlash doim to‘g‘ri bo‘lmaydi.
- Barcha yopiq ilovalarni qayta shakllantirish umumiy OS shell bilan kafolatlanmaydi.
- Ekran/sichqoncha/klaviaturani “butkul almashtirish” yo‘nalish, dalillangan mahsulot qiymati emas.
- Kundalik ishni tezlashtirish va kreativ samarani oshirish hozircha **tekshiriladigan gipoteza**.

## 10. Keyingi aniq vazifalar

- Bitta professional vazifani tanlash, hozirgi workflow va frictionni o‘lchash.
- Living Object va Intent modelining minimal formal kontraktini ishlab chiqish.
- Bitta aniq transformni, masalan data + vaqt → foydali tahlil obyektini, ishlatish.
- Kompozitsiya va foydalanish paytida cognitive load, accuracy, completion time hamda reuse'ni o‘lchash.
- Living OS va yangi hardware haqidagi qarorlarni asosiy gipoteza validatsiyasigacha ochiq qoldirish.

## Bog‘liq hujjatlar

- [Vision](../VISION.md)
- [Interaction principles](../design/interaction-principles.md)
- [Prototip bo‘yicha saboqlar](../design/prototype-feedback-2026-11-11.md)
- [Experiment 001](../experiments/001-object-composition.md)
- [Open questions](../open-questions.md)

---

*Ushbu hujjat suhbatdan ishlab chiqilgan konseptual taklif. Muallif niyatini imkon qadar aniq ifodalaydi, lekin hali tekshirilmagan arxitektura g‘oyalarini tasdiqlangan qaror deb ko‘rsatmaydi.*
