# Living — Research-first roadmap

**Holat:** PROPOSAL; formal tasdiqlangan product roadmap emas.  
**Eslatma:** vaqt va resurslar qo‘pol ssenariy; moliyaviy majburiyat yoki delivery va'dasi emas.

## Fazalar

### 0 — Konsept va falsifikatsiya

**Vazifa:** Living nimani yaxshilashi kerakligini aniq aytish; o‘xshash ilmiy ishlarni o‘rganish; qarshi dalillar yig‘ish.

**Deliverables:** vision, glossary, prior art, risk register, open questions, user problem statements.

**Gate:** kamida bitta aniq foydalanuvchi vazifasi bor; odatiy mavjud vositalarda aniq friction kuzatilgan.

### 1 — Direct manipulation prototype

**Vazifa:** living-native obyektlarni joylashtirish, shakllantirish, persist qilish va undo.

**Gate:** foydalanuvchi alohida editor ochmasdan obyekt bilan aniq ishlaydi; gesture chalkashligi o‘lchanadi.

### 2 — Semantic composition prototype

**Vazifa:** kamida ikki obyektning typed combination'dan yangi behaviorli obyektga aylanishi.

**Gate:** [Experiment 001](../experiments/001-object-composition.md) orqali vazifa bajariladi, correctness va usability isbotlanadi.

### 3 — Safety and persistence MVP

**Vazifa:** permission model, sandbox, snapshots, provenance, schema migration, local-first.

**Gate:** muhim ma'lumot yo‘qolishi va ruxsatsiz amallar uchun qabul qilinadigan darajadagi xavfsizlik; sinovlarda barqaror qayta foydalanish.

### 4 — Targeted desktop workspace

**Vazifa:** aniq bir segmentga mos native desktop runtime, external service adapters va accessibility.

**Gate:** retention, real foyda va maintenance cost dalillari mavjud.

### 5 — Optional OS-level evolution

**Vazifa:** own shell/compositor, developer integration/SDK, deeper OS controls.

**Gate:** oldingi fazalar bozor/texnik jihatdan muvaffaqiyatli; kernel kerakligi alohida asoslangan.

## 3 muqobil mahsulot strategiyasi

| Variant | Nima uchun? | Qarshi dalil |
|---|---|---|
| Research prototype | Yangi HCI modelini minimal xarajat bilan sinash | Daromad darhol bo‘lmasligi mumkin |
| Professional living workspace | Aniq takroriy ish muammosiga yechim | Butun OS falsafasi qisman cheklanadi |
| Developer SDK | Boshqa ilovalarga Living objekti imkoniyatini berish | Vaqtidan oldin ekotizim yaratish qiyin |

**Hozirgi tavsiya:** 1 → 2 → 3; mahsulot segmenti foydalanuvchi tadqiqoti natijasidan keyin tanlansin.

## Jamoa va vaqt taxmini

| Faza | Odamlar (taxmin) | Davomiylik (taxmin) |
|---|---:|---:|
| Discovery | 1–3 | 4–8 hafta |
| PoC | 2–4 | 2–4 oy |
| MVP | 4–8 | 6–12 oy |
| Desktop | 8–15+ | 1–3 yil |
| OS ecosystem | Keng jamoa | Ko‘p yil |

Bu ssenariylar mustaqil o‘rtacha qiymat emas; texnik va UX murakkabligi vaqtni ko‘paytirishi mumkin.

## Kerakli ekspertiza

- Human-computer interaction va user research
- Interaction design va accessibility
- Graphics/rendering/runtime engineering
- Programming languages, types, schema evolution
- Security, sandboxing, permission mediation
- Storage/sync/local-first systems
- AI integration, evaluation, failure analysis
- Product discovery va distribution

## Qayta baholash mezonlari

- Agar demo real vazifada ishlamasa: konsepsiyani qisqartirish yoki rad etish.
- Agar foydalanuvchi ko‘p chat va debugging qilishga majbur bo‘lsa: directness gipotezasini qayta ko‘rish.
- Agar yangi obyektlar qayta ishlatilmasa: retention va product-value farazini tekshirish.
- Agar mavjud app'lar yetarlicha yaxshi bo‘lsa: faqat sezilarli yangi imkoniyat beradigan vazifaga fokuslanish.

**Roadmap qarori hali qabul qilinmagan.** GitHub'dagi “proposals” papkasi qabul qilingan qarorlarni emas, muqobillarni saqlaydi.
