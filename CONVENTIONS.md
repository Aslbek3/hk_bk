# Konvensiyalar

Bu repo — Obsidian ombori. Qoidalar qisqa va majburiy.

## Fayl nomi
- kichik lotin harflari, pastki chiziq, kengaytma `.md`
- bo'shliq, qavs, kirill, emoji yo'q
- personaj fayli — ism bilan: `agnes.md`
- sana prefiksi yo'q (u commit tarixida bor)

## Frontmatter (har faylda majburiy)

```yaml
---
status: canon
work: soya_hukmdori
updated: 2026-10-29
---
```

`status` qiymatlari:
- `canon` — foydalanuvchi tasdiqlagan, o'zgarmas
- `branch` — ochiq variant, hali tanlanmagan
- `rejected` — rad etilgan, qaytarilmaydi
- `proposal` — AI yoki boshqa manbadan kelgan, tasdiq kutayotgan
- `meta` — hujjatning o'zi haqida (konvensiya, indeks)

## Chegara qoidasi
1. Yangi g'oya **avval** `branch.md` ga tushadi. Hech qachon to'g'ridan-to'g'ri `kanon.md` ga yozilmaydi.
2. Foydalanuvchi "ha" desa — `branch.md` dan `kanon.md` ga ko'chiriladi, commit xabarida qayd etiladi.
3. Foydalanuvchi "yo'q" desa — `rejected.md` ga, sababi bilan.
4. `kanon.md` dagi qoidani AI o'zgartira olmaydi, faqat taklif qiladi.

## Papka
- papka — **asar** bo'yicha
- status papkada emas, frontmatter'da
- `_common/` — bir nechta asarga tegishli
- `_arxiv/` — xom matn, eksport, eski nusxalar (o'qish uchun emas)

## Commit xabari
`<asar>: <feat|fix|move>: <qisqa mazmun>`

Misol: `soya_hukmdori: feat: kotiba personaji qo'shildi`
Kanon o'zgarishi alohida: `soya_hukmdori: canon: ovoz berish qoidasi aniqlashtirildi`

## Taqiqlar
- bir mavzuni ikki faylda takrorlash
- `_common/` dan nusxa ko'chirish (havola ishlatiladi)
- xom matnni ildizda saqlash
- `status` siz fayl yaratish
