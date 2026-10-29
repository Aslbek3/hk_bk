# HK_BK — Obsidian Eslatmalar Arxivi

Telegram orqali yuklangan Obsidian eslatmalar to'plami. Badiiy asarlar
(romanlar/konseptlar) uchun g'oya, kanon, tarmoqlangan variant va tahlil
qoralamalarini saqlaydi.

Hozircha 4 ta asar bor: **Soya Hukmdori (Cid)**, **Abadiyat Qafasi**,
**Frederin**, **Free God**.

## Qayerdan boshlash

- 📖 **Mazmunni qidirayapsizmi?** → [00_index.md](00_index.md)
- ✍️ **Yangi fayl qo'shmoqchimisiz?** → [CONVENTIONS.md](CONVENTIONS.md) (nomlash, frontmatter, papka qoidalari)

## Tuzilma

```
Asarlar/<asar>/kanon.md | branch.md | rejected.md | variantlar/ | tahlil/
_common/      — bir nechta asarga baravar tegishli g'oyalar
_arxiv/       — xom suhbat matni va JSON eksportlar (dalil, o'qish uchun emas)
```

Har bir asar fayli boshida `status` (canon/branch/rejected/proposal/analysis),
`work` (asar nomi) va `updated` maydonlari bo'lgan frontmatter bor — bu
Obsidian Dataview orqali "barcha kanon qoidalar" kabi ro'yxatlarni avtomatik
chiqarish imkonini beradi.
