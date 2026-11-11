# Living Object Model — dastlabki konsepsiya

**Status:** Proposal / hali tasdiqlanmagan arxitektura.  
**Maqsad:** Obyektni shunchaki chiziladigan komponentdan funksional hisoblash birligiga aylantirish.

## Model

Har bir Living Object quyidagi qatlamlarga ega deb faraz qilamiz:

| Qatlam | Vazifa | Savol |
|---|---|---|
| **Identity** | Stable unique ID; referensiyalar | Bu aynan qaysi obyekt? |
| **Shape / presentation** | Geometriya, dizayn, vizual holat | Qanday ko‘rinadi? |
| **Data & state** | Strukturali ma'lumot, joriy qiymatlar | Nima saqlanadi? |
| **Behavior** | Reaksiyalar, hisoblash, qoida va amallar | Nima qila oladi? |
| **Typed capabilities** | Import/export, contracts, events | Nima bilan mos ulanadi? |
| **Permissions** | Resurslarga kirish cheklovi | Nimaga haqli? |
| **Provenance** | Kelib chiqish, bog‘lanish, versiya | Qanday hosil bo‘lgan? |

**Shape behavior emas.** Obyektni uchburchakka aylantirish uning ma'nosi yoki ishlashini o‘zgartirmasligi ham mumkin. UI transform va semantic transform alohida operatsiyalar sifatida aniqlanishi kerak.

## Obyekt grafigi

O‘zaro bog‘langan obyektlar faqat ekrandagi pozitsiyalar orqali emas, quyidagilar orqali ham bog‘lanadi:

- Data references: qaysi ma'lumot qayerdan keladi;
- Typed ports / contracts: qaysi qiymat va amallar mos;
- Transformation edges: qiymat qanday hisoblanadi;
- Dependency edges: bir obyekt yangilansa boshqasi qanday reaksiyaga kirishadi;
- Permission boundaries: har bir chekka qanday huquq talab qiladi;
- Provenance graph: natija qayerdan kelgan va qanday orqaga qaytariladi.

## Misol: Expenses + Calendar

- Expenses: valyuta, summa, transaction date, category, source.
- Calendar: sana oralig‘i, vaqt zonasi, event date.
- Composition engine: date field va timestamp mosligini tekshiradi; valyuta birliklarini nazorat qiladi.
- Taklif qilinadigan yangi obyekt: “Expenses over time”.
- Yangi behavior: filtr, agregatsiya, chart, vaqt bo‘yicha solishtirish.
- Yangi obyekt source obyektlar bilan data lineage'ni saqlaydi va ishlashni davom ettiradi.

Bu **deterministik tor use-case**. Bundan “istalgan ikkita obyekt birlashishi mumkin” degan xulosa chiqmaydi.

## Composition pipeline — proposal

1. Intent discovery: foydalanuvchi obyektlarni yaqinlashtiradi yoki ulaydi.
2. Schema/capability introspection: input/output, data turlari, units, permissions olinadi.
3. Deterministic matching: oldindan aniqlangan semantik qoidalar tekshiriladi.
4. Ambiguity handling: noaniq bo‘lsa AI variantlarni **taklif qiladi**, foydalanuvchi tanlaydi.
5. Preview: sample data va kutiladigan o‘zgarishlar ko‘rsatiladi.
6. Execution: permission boundary va runtime validation.
7. Persist: yangi obyekt, history, provenance, version.
8. Revert/split: odatda qaytish mumkin; tashqi irreversible actions alohida xavf sinfi.

## Xavfsizlik kontrakti

- Default-deny: yangi obyekt barcha resurslarga avtomatik kira olmaydi.
- Tashqi amallar (email, file delete, network transfer) uchun aniq ruxsat.
- Dinamik behavior sandbox/quotas/timeouts ostida ishlaydi.
- Dasturiy kodni tushunarli explanation, test va logs bilan kuzatish kerak.
- Composition permissions'ni ko‘paytirib yubormasligi kerak: yangi obyektga faqat kerakli huquqlar beriladi.

## Boshlang‘ich amalga oshirish variantlari (tanlanmagan)

- Typed graph + stable IDs + schema evolution.
- Declarative behavior DSL/IR (sinov uchun osonroq) yoki sandboxed WebAssembly components.
- Event-log + snapshots; local-first.
- Canvas yoki native renderer ustida scene graph.

Typed interfaces uchun [WASM Component Model](https://component-model.bytecodealliance.org/design/components.html) relevant, lekin semantik ma'no muammosini o‘zi hal qilmaydi.

## Tekshirilishi kerak bo‘lgan farazlar

- H1: oddiy foydalanuvchi obyektning data va behavior mohiyatini developer terminlarisiz tushuna oladi.
- H2: tor domenda typed data asosida kompozitsiyalar predictably foydali chiqadi.
- H3: preview + explanation noaniqlik va xavfni kamaytiradi.
- H4: foydalanuvchi kompozitsiya qilgan obyektni keyin qayta ishlatadi.

Bular uchun [Experiment 001](../experiments/001-object-composition.md) boshlang‘ich sinov.
