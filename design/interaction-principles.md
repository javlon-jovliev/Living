# Living — Interaction Principles (draft)

**Holat:** Design hypothesis. Tasdiqlangan UI kit, prototip yoki hardware spesifikatsiyasi emas.  
**Sana:** 2026-11-12

## Asosiy UX savoli

**Inson niyatini ma'lum bir dastur, menyu, qoida yoki coding skill o‘rganmasdan qanday qilib hisoblash natijasiga aylantira oladi?**

Living'ni “AI desktop UI” yoki “Minecraft for productivity” ko‘rinishiga keltirish g‘oyani cheklaydi. Interface o‘zini ko‘rsatishdan ko‘ra insonning real ishini bajarishga yordam berishi kerak.

## Kerakli tajriba sifatlari

1. **Directness:** obyekt ustidagi harakat natijani shu joyning o‘zida ko‘rsatsin.
2. **Malleability:** foydalanuvchi layoutdan tashqari ma'lumot, munosabat va funksiyani ham o‘zgartira olsin.
3. **Calmness:** bo‘sh joy, fokus, kam vizual shovqin; barcha imkoniyatlar bir vaqtda ko‘rinishi shart emas.
4. **Continuous creation/use:** yaratish va foydalanish o‘rtasida majburiy alohida “editor” dunyosi bo‘lmasin.
5. **Predictability:** harakat oldidan affordance/preview; foydalanuvchi nima bo‘lishini oldindan taxmin qila olsin.
6. **Explainability:** yangi obyekt qaysi ma'lumotlar, funksiyalar va ruxsatlardan hosil bo‘lganini ko‘rsatish.
7. **Device flexibility:** sichqoncha/klaviatura/ekran — hozirgi input vositalari, lekin model ularga bog‘lanib qolmasin.
8. **Functional minimalism:** bitta aniq vazifa, bir nechta haqiqiy obyekt; UI'ni to‘ldirish uchun dekorativ element qo‘shilmasin.
9. **Reversibility:** tasodifiy transformlar tuzatilishi; irreversible tashqi amallar alohida qaror bo‘lsin.
10. **Accessibility:** faqat gesture yoki VR bilan ishlash majburiy emas; keyboard, screen reader, motor accessibility hisobga olinsin.

## Muhim dizayn trade-offlari

| Qarama-qarshilik | Dastlabki yondashuv |
|---|---|
| Editing vs using | Kontekstual affordance, preview, lock, undo; “editor yo‘q” = “niyat ajratilmaydi” emas |
| Freedom vs predictability | Qat'iy ichki semantik kontrakt; moslashuvchan tashqi ko‘rinish |
| AI magic vs trust | Tushunarli variantlar, provenance, test va approval |
| 2D vs 3D | Vazifa qaysi biridan foyda olishini sinash; butun UI'ni 3D qilish shart emas |
| Physical metaphor vs abstract logic | Fizikaga o‘xshash harakat faqat tushunarli joyda; shartlar/trigger uchun mos boshqa ifoda |
| Personalization vs onboarding | Ishga tayyor boshlang‘ich muhit, keyin chuqur moslashish |
| Hardware novelty vs productivity | Avval real vazifada foyda; keyin yangi apparat |

## Birinchi prototip uchun talab

- **Bir vaqtning o‘zida bitta real vazifa.**
- Obyektlar real ma'lumot va tekshiriladigan hisoblash imkoniyatiga ega bo‘lsin.
- Foydalanuvchi bir amal bilan obyektning ma'noli parametrini o‘zgartira olsin.
- Ikki obyektning birlashishi **faqat vizual grouping emas**, yangi hisoblash natijasini hosil qilsin.
- Kelib chiqishi, nima bajarilgani va qanday ajratish mumkinligi tushunarli bo‘lsin.
- Doimiy AI chat, sidebar, toolbar, fon rasmi yoki kartochka har doim shart emas.
- UI keng maydon va joyida paydo bo‘ladigan affordance bilan ifodalansin; katta funktsional ro‘yxatni birdan ko‘rsatmasin.
- Prototip vazifa yakunini ko‘rsatsin; faqat konseptual obyektdan iborat stsenografiya bo‘lmasin.

## Prototipni baholash

- Foydalanuvchi ko‘rsatmasiz vazifani tushundimi?
- Obyektni qanday ishlatish va qanday o‘zgartirishni adashtirdimi?
- Yangi obyektning **nima qilishi** unga tushunarlimi?
- Natijani tekshira oladimi?
- Baseline vositadan tezroq/foydaliroqmi?
- Keyin shu natijaga qaytdimi?

## Vizual yo‘nalishni ochiq qoldirish

Hozircha quyidagilar yakuniy qaror emas: flat/3D/AR, volumetric UI, skeuomorphism, gesture vocabulary, vizual fizik kuchlar, AI overlay, yangi kompyuter apparati.

Suhbatdagi vizual prototiplardan olingan xulosalar: [Prototype feedback](prototype-feedback-2026-11-11.md).
