# Living — Risk Register

**Sana:** 2026-11-11  
**Holat:** Dastlabki xavf modeli; darajalar ekspert taxmini. “Mitigation” xavfni to‘liq yo‘qotishini anglatmaydi.

| ID | Xavf | Muhimlik | Mitigatsiya / sinov | Qoldiq noaniqlik |
|---|---|---|---|---|
| R01 | **Semantik kompozitsiya**: obyektlarning birlashishi foydasiz ma'no beradi | Kritik | Typed contract, domain rules, AI alternatives, preview, user choice | Har doim to‘g‘ri niyatni bilish imkonsiz |
| R02 | **Generatsiya qilingan behavior**: xato yoki zararli kod | Kritik | Sandboxed runtime, default deny, test, signing, audit, quotas | Side effects, supply chain |
| R03 | **Data privacy / exfiltration** | Kritik | Granular permissions, network isolation, explicit destination confirmation | User consent fatigue |
| R04 | **Accidental edits**: gesture niyati chalkash | Yuqori | Affordance, previews, snapshots, undo, lockable objects | O‘rganish xarajati |
| R05 | **Data/schema interoperability** | Yuqori | Typed schemas, units, adapters, migrations, provenance | Semantik ziddiyat |
| R06 | **State loss / conflict** | Yuqori | Local-first history, snapshots, deterministic replay, sync tests | Semantik merge nizolari |
| R07 | **Third-party app limits** | Yuqori | Living-native, documented API adapter, external app fallback | Yopiq app'lar to‘liq malleable bo‘lmaydi |
| R08 | **UX complexity** | Yuqori | Progressive disclosure, real user research, conventional fallback | Foydalanuvchilar customizatsiyani xohlamasligi |
| R09 | **Accessibility** | Yuqori | Semantik fokus, keyboard actions, screen reader labels | Arbitrary spatial layout |
| R10 | **Performance and latency** | O‘rta-yuqori | Local rendering, caching, async AI, deterministic core | Katta obyekt graph |
| R11 | **Maintenance explosion** | Yuqori | Version pinning, reproducible transformations, tests, traces | Har user'ning noyob muhiti |
| R12 | **Adoption/ecosystem** | Kritik (biznes) | Single high-value segment, measurable benefit, gradual integrations | Network effects, migration cost |
| R13 | **Research bias** | Yuqori | Falsifiable hypotheses, counterexamples, negative results log | Founder/AI optimism bias |
| R14 | **Public IP/privacy leakage** | O‘rta-yuqori | Review before publication; keep confidential items out of public repo | Public git history persistent |

## Kritik ajratishlar

**Code isolation vs permission:** WebAssembly o‘zi avtomatik ravishda hamma xavfni bartaraf qilmaydi. Capability policy, network/filesystem mediator va runtime konfiguratsiyasi shart.

**Undo vs real-world side-effect:** UI holatini qaytarish mumkin, lekin yuborilgan xat yoki o‘chirilgan masofaviy faylni odatda avtomatik qaytarib bo‘lmaydi. Bunday amallar ikki bosqichli tasdiq va alohida auditga ega bo‘lishi kerak.

**Local-first vs bug-free:** offline storage va CRDT konfliktlarni kamaytirishi mumkin, lekin noto‘g‘ri semantic transform va logic xatosini o‘zi tuzatmaydi.

**Universality vs predictable operation:** foydalanuvchi istagan cheksiz kombinatsiya bilan ishonchli, o‘rganiladigan interaksiya o‘rtasida trade-off mavjud.

## Tadqiqot vazifalari

- Threat model: permissions, AI prompt injection, untrusted imports, unsafe side effects.
- Semantic schema test: valyuta, birlik, locale, timezone, missing data.
- Accessibility walkthrough: keyboard-only, screen reader, reduced motion.
- UX test: move vs resize vs link vs behavior edit ambiguity.
- System test: snapshot/undo, crash recovery, object graph migration, sync.

## Manbalar

- [WebAssembly Component Model](https://component-model.bytecodealliance.org/design/components.html)
- [XDG Desktop Portal security model](https://flatpak.github.io/xdg-desktop-portal/docs/security-model.html)
- [Automerge conflicts](https://automerge.org/docs/reference/documents/conflicts/)
- [W3C WCAG Focus Order](https://www.w3.org/WAI/WCAG22/Understanding/focus-order.html)

Alohida kuzatiladigan masalalar: [Ochiq savollar](../open-questions.md).
