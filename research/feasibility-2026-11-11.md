# Living — Feasibility & Strategic Assessment

**Sana:** 2026-11-11  
**Turi:** Research synthesis + expert assessment  
**Status:** Dastlabki baho. Foydalanuvchi sinovi, audit yoki tijoriy validatsiya emas.

## Executive summary

Living'ning asosiy interaksiya shakli va tor domenli funksional kompozitsiyasi bugungi texnologiyalar bilan qurilishi mumkin. Biroq **istalgan ikki obyektning istalgan foydali funksiyaga o‘z-o‘zidan aylanishi** prinsipial semantik noaniqlikka ega. Barcha yopiq uchinchi tomon dasturlarini ichidan o‘zgartiradigan universal OS ham tayyor umumiy mexanizm emas.

**Strategik baho:** avval native obyektlar asosidagi Living Workspace; foyda va xavfsizlik isbotlangach desktop shell/OS integration. Yangi kernel — erta boshlanish uchun iqtisodiy asoslanmagan.

## Uch darajadagi realizm

| Daraja | Nima mumkin? | Baholash |
|---|---|---|
| 1. Living Workspace | Native obyektlarni ushlab o‘zgartirish, typed composition, yangi behavior, persistence, history | Bugun muhandislik jihatdan amalga oshiriladi |
| 2. Living Desktop Environment | Lokal dastur shell/runtime, OS API, ruxsatli integratsiyalar va offline foydalanish | Qiyin, lekin texnik jihatdan asosli maqsad |
| 3. Universal Living OS | Istalgan obyekt va yopiq dastur elementlarini cheksiz semantik o‘zgartirish | Hozircha isbotlanmagan; talab va muhandislik chegaralari ochiq |

Bu baholar ehtimollik foizlari emas, texnik cheklovlar bo‘yicha sifatli hukm.

## Texnik tayyorlik

**Bugun mavjud bo‘lgan asboblar:**
- Canvas, scene graph, custom shape, transformatsiya, grafika.
- Lokal database, event log, obyekt identifikatori, snapshot.
- Type-checked interfeyslar va modulli runtime.
- Sandboxing va OS resurslariga ruxsatni ajratish.
- AI yordamida yangi konfiguratsiya/behavior taklif qilish.

**Hali Living uchun o‘zi hal bo‘lmaydigan masalalar:**
- Foydalanuvchi harakatining **niyatini** aniqlash.
- Birlashtirishning **ma'nosini** ishlab chiqish va tekshirish.
- AI generatsiyasini xavfsiz va tushunarli qilish.
- Barcha obyektlar uchun ma'lumotlar turlari, birliklar va semantik moslik.
- Har bir foydalanuvchining o‘zgaruvchan muhitini test qilish va servis qilish.
- Tashqi yopiq ilovalar bilan chuqur integratsiya.

## Asosiy ilmiy nuqta

**Type compatibility != semantic usefulness.**

Masalan, xarajatlar va sanalar mos typed data berishi mumkin; tizim vaqt bo‘yicha xarajat grafikini deterministik yaratadi. Ammo “xarita + musiqiy pleyer” bir nechta ma'noli natijaga ega: joyga mos musiqa, geografik musiqiy xotira yoki marshrut soundtreki. Input turlarining mosligi inson xohishini hal qilmaydi.

Taklif: aniq kombinatsiyalarda deterministik qoidalar; noaniq kombinatsiyalarda AI bilan variant yaratish + preview + tanlash + ruxsat + rollback. Bu hali tajriba bilan validatsiyalanmagan.

## Qanchalik foydali?

**Potensial foyda, isbot emas:**
- Bir nechta vositadagi ma'lumot va funksiyani bitta shaxsiy workflow'ga birlashtirish.
- Maxsus hisobot va vizualizatsiyalarni har safar dasturchidan so‘ramasdan yaratish.
- Saqlanadigan, qayta ishlatiladigan, ma'lumotga bog‘langan hisoblash obyektlari.
- Uzoq muddat o‘z ishiga moslashadigan makon.

**Buning qarshi dalili:** foydalanuvchilarning ko‘pi UI yasashni emas, ishni tez bitirishni istaydi. Yangi UI'ni qo‘lda yoki AI bilan yaratish oddiy app'da ishlashdan qimmatga tushishi mumkin.

**Dastlab sinashga arziydigan segmentlar (hypothesis):** tadqiqotchilar, analitiklar, ko‘p manbali hujjat/data bilan ishlovchilar, texnik-kreativ mutaxassislar. Universal consumer OS uchun talab to‘g‘ridan-to‘g‘ri o‘lchanmagan.

## Muqobil yo‘llar

| Yo‘l | Kuchli tomoni | Zaif tomoni |
|---|---|---|
| Browser canvas prototip | Tez iteratsiya, HCI sinovlari uchun qulay | OS integratsiyasi cheklangan |
| Native desktop app / shell | Local-first, yanada chuqurroq resurslar | Portlash darajasidagi integratsiya va maintenance |
| Linux Wayland shell | Tizim darajasidagi user experience | Yopiq ilova ichki UI'ni avtomatik ochmaydi |
| Yangi OS kernel | Nazariy chuqur nazorat | Yadro muammosini hal qilmaydigan katta investitsiya |

**Muhim:** browser prototip sinov vositasi, Living mahsuloti “website bo‘lishi kerak” degan qaror emas.

## Jamoa va muddat — faraziy reja

| Bosqich | Mutaxassis | Taxminiy vaqt | Isbot mezoni |
|---|---:|---:|---|
| Discovery | 1–3 | 4–8 hafta | Real foydalanuvchi muammosi topiladi |
| PoC | 2–4 | 2–4 oy | 2–3 kompozitsiya ishni yakunlaydi |
| MVP | 4–8 | 6–12 oy | Xavfsiz takroriy foydalanish |
| Desktop platform | 8–15+ | 1–3 yil | Ishlash barqarorligi, integratsiya |
| OS ecosystem | Katta jamoa | Ko‘p yil | Developer ecosystem va migration |

Bu bozor o‘rtachasi yoki va'da emas. Jamoa tajribasi, scope va yondashuvga qarab o‘zgaradi.

**Budjet modelining misoli:** 5 mutaxassis x 12 oy x $10 000 fully-loaded = $600 000; bu faqat arifmetik ssenariy, lokal ish haqi statistikasi emas.

## Bozor / raqobatga doir ehtiyotkor xulosa

Figma, Bubble, Lovable, v0 kabi mahsulotlar moslashuvchan UI va app creation'ga talab borligi haqida qisman signal beradi; **Living universal OS uchun talabni isbotlamaydi**. Platformani almashtirish mahsulotdan foydalanishga qo‘shimcha migratsiya, compatibility va network-effects xarajatini olib keladi.

Mumkin biznes yo‘llari (hypothesis): mutaxassislar uchun professional workspace, open-core + collaboration/sync, tashkilot integratsiyalari, developer SDK. Monetizatsiya hali tekshirilmagan.

## Tavsiya etilgan ketma-ketlik

1. Obyekt modelini va foydalanuvchi vazifasini aniqlash.
2. 4–6 Living-native obyektli prototip.
3. Birlashtirishdan yangi foydali behavior chiqarish.
4. Preview, rollback, permissions.
5. Baseline bilan foydalanuvchi testi.
6. Foyda bo‘lsa runtime'ni ajratish va desktopga o‘tish.
7. Keyin SDK/OS darajasi haqida qaror.

## Ishonch darajasi va cheklovlar

- **Yuqoriroq ishonch:** mavjud grafik, persistent state va typed komponentlar qurilishi mumkin.
- **O‘rta ishonch:** muayyan domenlarda AI + typed composition foydali bo‘lishi mumkin.
- **Past ishonch:** universal semantik kompozitsiya va mass-market OS adoption.
- **Dalil yetishmaydi:** real user retention, ish unumdorligi, willingness to pay va xavfsizlik auditi.

Ilmiy asoslar: [Prior art](prior-art.md) · [Manbalar](sources.md)  
Amaliy xavflar: [Risk register](../risks/risk-register.md) · [Eksperiment 001](../experiments/001-object-composition.md)
