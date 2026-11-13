# Living — niyatni harakat orqali ifodalash

**Sana:** 2026-11-13  
**Holat:** Suhbatdan kelib chiqqan gipoteza va tajriba taklifi. Sinov natijalari hali yo‘q.

Bu qayd [oldingi konseptual suhbat](conversation-findings-2026-11-11.md) va [interaksiya tamoyillari](../design/interaction-principles.md) ustiga quriladi.

## Tadqiqot savoli

Odam fikrini gapga aylantirmasdan, ish obyektlarini chizish, tanlash, guruhlash yoki o‘zgartirish orqali kompyuterga qanchalik aniq ifodalay oladi? Living shu amallardan foydalanuvchi tekshira oladigan hisoblashni taklif qila oladimi?

Bir harakatning ma’nosi kontekstga bog‘liq. Ikki hujjatni yonma-yon qo‘yish ularni taqqoslash, birlashtirish yoki shunchaki bir vaqtda ko‘rish istagini anglatishi mumkin. Harakatni aniq qayd etish bu talqinlardan qaysi biri to‘g‘ri ekanini aniqlashga yetmaydi. Ba’zan maqsadning o‘zi ham natija ko‘ringandan keyin shakllanadi.

## Niyatni ifodalash vositalari

| Signal | Ish jarayonidagi vazifasi |
|---|---|
| Ko‘rsatish yoki tegish | Qaysi obyekt yoki bo‘lim ustida ishlash kerakligini bildiradi. |
| Eskiz, joylashtirish yoki bog‘lash | Kerakli shakl, tartib yoki munosabatni ko‘rsatadi. |
| Misol va qarshi misol | Toifaga nimalar kirishi va qaysi holat istisno ekanini ko‘rsatadi. |
| Amalni bajarib ko‘rsatish | Tizim boshqa obyektlarda takrorlab ko‘rishi mumkin bo‘lgan ish ketma-ketligini beradi. |
| Natijani tanlash, o‘zgartirish yoki qaytarish | Tizim talqinini tekshirish va aniqlashtirishga yordam beradi. |
| Nigoh va joriy kontekst | E’tibor qaratilgan obyektlarni aniqlashga va ehtimoliy talqinlarni toraytirishga yordam beradi. Nigohning o‘zi tasdiqlash uchun zaif signal. |

Matn yoki nutq ham shu vositalarga qo‘shilishi mumkin. Masalan, odam ikki obyektni ko‘rsatib, «Shularni solishtir» deydi. Ko‘rsatish obyektlarni aniqlaydi, so‘z esa amalni belgilaydi.

## Interaksiya taklifi

1. Odam obyektlar ustida ishlaydi yoki misol ko‘rsatadi.
2. Living harakat va joriy vazifadan kelib chiqib, hisoblashning tahrirlanadigan dastlabki natijasini ko‘rsatadi. Agar ikki talqin turli natija bersa, farq ko‘rinadigan misolni chiqaradi.
3. Odam natijani bevosita tuzatadi. Living o‘z talqinini yangilab, qaysi qoida natijani hosil qilganini ko‘rsatadi.
4. Odam qoidani saqlasa, tizim shu hisoblashni mos tuzilishdagi yangi ma’lumotda bajaradi. Xuddi shu qoidani keyin tekshirish va tahrirlash mumkin.

AI talqin yoki muqobil variant taklif qilishi mumkin. Tasdiqlangan qoida bo‘yicha hisoblash va natijani qayta ko‘rsatish prototipning hisoblash qismiga tegishli.

## Xarajatlar prototipida sinash

[Experiment 002](https://github.com/javlon-jovliev/Living/pull/2) ikki oldindan belgilangan kompozitsiyani namoyish qiladi. Keyingi taklif odam o‘zi ko‘rsatgan misollardan yangi qoida hosil qila olishini tekshiradi.

Masalan, odam Spotify, internet va bulut xotirasi to‘lovlarini bitta guruhga suradi. Living ikkita talqinni ko‘rsatadi — «takroriy to‘lovlar» va «xizmat obunalari». Birinchi variantda ijara ham chiqadi. Odam ijarani guruhdan chiqarib, qaysi talqin mosligini ko‘rsatadi. Tasdiqlangan qoida grafikni yangilaydi va keyingi CSV fayliga qo‘llanadi. Misollar bir nechta qoidaga mos kelishi mumkinligi sababli foydalanuvchi tizim taklif qilgan qoidani ko‘rib, uning yangi yozuvlarda qanday ishlashini tekshiradi.

**Gipoteza.** Ishlayotgan natijani bevosita tahrirlash odamga noaniq maqsadni tezroq aniqlashtirish va uni qayta ishlatiladigan hisoblashga aylantirishda yordam beradi.

**Sinov taklifi.** Bir xil model va ma’lumot bilan chat hamda Living’da «Xarajatlar nega oshdi?» vazifasini bering. Ishtirokchi o‘z mezonini topishi uchun ketgan vaqtni, noto‘g‘ri talqinlarni tuzatishga ketgan amallarni va yangi CSV kelganda hisobni mustaqil moslay olishini kuzating. Natija o‘xshash chiqsa yoki Living’da ko‘proq tuzatish talab qilinsa, ushbu vazifada gipoteza qo‘llab-quvvatlanmaydi. Keyingi savol — shu yondashuv boshqa turdagi ishda, masalan, hujjatlarning tanlangan bo‘limlarini taqqoslashda ham foyda beradimi?

## Oldingi ishlar

- Kirsh va Maglio Tetris tajribasida ayrim harakatlar masalani yechishni osonlashtirishini ko‘rsatgan. Bu harakat fikrni shakllantirishga yordam berishi mumkinligiga misol. [Epistemic action, 1994](https://doi.org/10.1016/0364-0213(94)90007-8)
- Horvitz avtomatlashtirish va obyektlarni bevosita boshqarishni birlashtirish tamoyillarini ta’riflagan. [Mixed-initiative interfaces, 1999](https://www.microsoft.com/en-us/research/publication/principles-mixed-initiative-user-interfaces/)
- Bolt nutq va ko‘rsatish orqali grafik obyektlarga murojaat qilishni namoyish qilgan. Cypher’ning Eager tizimi takrorlanayotgan ishda tizim keyingi qadamni qanday taxmin qilganini ko‘rsatgan. [Put-That-There, 1980](https://doi.org/10.1145/800250.807503) · [Eager, 1991](https://www.acypher.com/Publications/CHI91/EagerCHI.html)
- Ishii va Ullmer jismoniy obyektlar orqali raqamli ma’lumotni boshqarishni prototiplarda o‘rgangan. Bu yo‘nalish sensorli stol yoki jismoniy obyektlar qachon qo‘shimcha ifoda imkonini berishini sinash uchun asos bo‘la oladi. [Tangible Bits, 1997](https://www.media.mit.edu/publications/tangible-bits-towards-seamless-interfaces-between-people-bits-and-atoms-2/)
