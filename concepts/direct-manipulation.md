# Bevosita shakllantirish: interaksiya modeli

**Status:** Research proposal, usability bilan tekshirilmagan.

## Asosiy paradoks

“Editor kerak emas” degani **tahrirlash niyatini ajratish kerak emas** degani emas.

Bir obyektni tortish quyidagilarni anglatishi mumkin:
- Obyektni fazoda ko‘chirish;
- Obyekt shaklini cho‘zish;
- Undagi qiymatni o‘zgartirish;
- Boshqa obyekt bilan bog‘lash;
- Yangi funksiya yaratish.

Noto‘g‘ri talqin foydalanuvchi ishonchini yo‘qotadi.

## Candidate interaction grammar

| Harakat | Taxminiy ma'no | Xavf |
|---|---|---|
| Body drag | Move | Ichki qiymatni tahrirlash bilan chalkashadi |
| Edge/corner drag | Resize/reshape | Ma'lumot yo‘qolishi yoki layout buzilishi |
| Connection affordance | Link/compose | Noto‘g‘ri semantik ulanish |
| Object split gesture | Divide structure | State/provenance qay darajada bo‘linishi noaniq |
| Hold/hover | Preview edit affordance | Touch va accessibility mosligi |
| Undo/restore | Revert | External side effect qaytmasligi mumkin |

Bular tayyor standart emas. Qaysi interaction primitive eng tushunarli ekanini kuzatuv bilan topish kerak.

## UX xavfsizlik qoidalari

1. Object action va object-edit niyati ko‘rinib tursin; majburiy alohida “builder” rejimi bo‘lmasin.
2. Har bir kompozitsiya amalga oshishidan oldin tushunarli preview taqdim etilsin.
3. Yangi behavior yaratish bilan tashqi amallarni ishga tushirish bir xil amal bo‘lmasin.
4. Undo/redo, snapshots va reset to stable state asosiy OS tajribasining bir qismi bo‘lsin.
5. Focus order va semantik accessibility grafik joylashuvga to‘liq bog‘lanmasin.
6. AI noaniqlikni yashirmasin; variantlarni tasdiqqa taklif qilsin.

## O‘rganish qiyaligi

Boshlang‘ich makon foydali bo‘lishi, foydalanuvchi barcha imkoniyatni oldindan bilishi shart bo‘lmasligi kerak. Oddiy foydalanishdan kichik o‘zgartirishga, undan yangi obyekt yaratishga o'tish bosqichma-bosqich bo‘ladi.

Bu “gentle slope from user to creator” g‘oyasiga yaqin: [Ink & Switch, Malleable Software](https://www.inkandswitch.com/essay/malleable-software/).

## O‘lchash

- Intent recognition rate: foydalanuvchi qilmoqchi bo‘lgan amal tushunarli bajariladimi?
- Accidental changes: necha marta xato transform yuz berdi?
- Recovery: xatoni foydalanuvchi qanchada tuzatdi?
- Learnability: 15–30 daqiqadan keyin mustaqil foydalanadimi?
- Accessibility: keyboard-only va assistive technology bilan vazifa bajariladimi?

Manba: [W3C Focus Order](https://www.w3.org/WAI/WCAG22/Understanding/focus-order.html).
