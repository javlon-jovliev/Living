# Living — ochiq savollar

**Holat:** Active research backlog. Javoblar topilgan deb hisoblanmaydi.  
**Prioritetlar:** P0 = fundamental, P1 = platforma uchun muhim, P2 = kelajak.

## P0 — Living paradigmasini isbotlaydigan savollar

1. Obyektni oddiy ishlatish bilan shakllantirishni foydalanuvchi qanday ajratadi? → HCI study / [direct manipulation](concepts/direct-manipulation.md).
2. Living Object'ning minimal semantik modeli qanday? → [object model](concepts/living-object-model.md) / formal specification.
3. Ikkita obyekt qo‘shilganda qaysi behavior tug‘ilishi foydalanuvchi niyatiga mosligini qanday bilamiz? → Semantic composition experiment.
4. Yangi funksional obyektni tushunish va tekshirish foydalanuvchidan qancha kuch talab qiladi? → Usability study.
5. Real ish samaradorligi standart vositaga nisbatan yaxshilanadimi? → [Experiment 001](experiments/001-object-composition.md).
6. “Alohida editor yo‘q” talabini accidental edit'larni oshirmasdan qanday bajarish mumkin? → Gesture tests.
7. Yangi behaviorlarni AI kodiga to‘liq ishonmasdan qanday ifodalaymiz? → Declarative IR vs sandboxed code.
8. Obyekt kompozitsiyasi permissions'ni kutilmagan tarzda ko‘paytirmasligiga qanday kafolat beramiz? → Security threat model.

## P1 — Platformaga o‘tish savollari

9. Living-native va external app obyektlari qanday universal API bilan aloqa qiladi?
10. Stable ID, schema migration va provenance qanday saqlanadi?
11. Undo/branch/snapshot interaktiv o‘zgarishlarni va yangi behaviorni qay darajada qaytara oladi?
12. Foydalanuvchi versiyalari ko‘payganda debugging, update va compatibility qanday ishlaydi?
13. Tarmoq bo‘lmaganda local-first ishlash, keyin sync qilish uchun qaysi consistency model mos?
14. Ekranni bebasga qayta shakllantirish bilan keyboard focus va screen reader tartibi qanday uyg‘unlashadi?
15. Qaysi chegaradan keyin native runtime browser canvasdan afzal bo‘ladi?
16. Xavfsizlik ruxsatlari va explanation UI'da qanday tushunarli ko‘rsatiladi?
17. Ma'lumot turlari, birliklar, vaqt zonalari va data provenance qanday standartlashadi?

## P2 — Mahsulot, bozor va ekotizim

18. Birinchi asosiy auditoriya kim: tadqiqotchi, analitik, knowledge worker yoki boshqalar?
19. Kim Living uchun muntazam pul to‘lashga tayyor; nimaga aynan?
20. Yangi obyekt yaratish uchun creator/developer ekotizimi kerak bo‘ladimi?
21. Personal space qurilmalardan tashqari ko‘chma bo‘lishi kerakmi?
22. Living boshqa OS'ning shell'i bo‘lib boshlanib, keyin mustaqil distribusiyaga o‘ta oladimi?
23. Ommaviy foydalanuvchi haqiqatan UI'ni doim o‘zgartirishni xohlaydimi?
24. Noyob personal space'larni boshqalarga tushuntirish va hamkorlik qanday ishlaydi?

## Qarshi savollar

- Living mavjud spreadsheet + automations + plugins'dan aniq qaysi vazifada yaxshiroq?
- Agar AI faqat bir necha aniq domenlarda ishlasa, bu hali Living hisoblanadimi?
- Vizual “loy kabi” interfeys kognitiv jihatdan ba'zi vazifalarda yomonroq bo‘lishi mumkinmi?
- Foydalanuvchi erkinligi ortganda himoya darajasini pasaytirmay turib qanday progressiv imkoniyat beramiz?
- Eng qimmat OS/desktop ishlari yadro gipotezasiga umuman bog‘liq bo‘lmasligi mumkinmi?

## Yangi savollar (2026-11-11 suhbatidan)

- Birinchi foydalanuvchi kim va uning har kuni takrorlanadigan qaysi ishi tanlanadi?
- Maqsad tadqiqot g‘oyasini isbotlashmi yoki daromad keltiradigan mahsulotmi?
- Muhit oddiy ekran uchunmi yoki VR/AR uchunmi?
- Qaysi fizik xususiyat (o‘lcham, temperatura, og‘irlik, rang) qaysi ma'noga tabiiy mos keladi? → [Fizik muhit](concepts/physical-environment.md)
- Komponentning "valentligi"ni kim belgilaydi: yasagan odammi, AI'mi? Xato qanday aniqlanadi?
- Foydalanuvchi quruvchi bo‘lishi kerakmi yoki AI taklifini tuzatuvchi tahrirchimi? → [Market evidence](research/market-evidence-2026-11.md)
- Qo‘l bilan ifodalab bo‘lmaydigan narsalar (shart, "doim", "xat kelganda") qanday kiritiladi? → [Fizik harakat chegaralari](concepts/physical-actions-limits.md)
- Muhit odamning mavjud ma'lumotiga (pochta, fayl, kalendar) qanday ulanadi?
- Tayyor komponentlar bazasida sifat va xavfsizlikni kim tekshiradi?

## Savolga javob berish qoidasi

Har bir savol keyinchalik ma'lum sinovga bog‘lanadi: **hypothesis → method → evidence → limitations → decision**. “AI buni qilishi mumkin” — mustaqil ilmiy dalil emas.

Manbalar: [Research register](research/sources.md) · [Risks](risks/risk-register.md).
