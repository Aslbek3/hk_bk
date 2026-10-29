# Konventsiyalar (Nomlash, Frontmatter, Commit)

Bu hujjat repo ichida ishlash qoidalarini belgilaydi. Mazmunni qidirsangiz
[00_index.md](00_index.md) ga, umumiy tavsif uchun [README.md](README.md)
ga qarang.

## 1. Papka tuzilmasi

```
Asarlar/<asar_slug>/
  kanon.md        — o'zgarmas, tasdiqlangan asoslar
  branch.md       — muhokama qilingan variantlar, ochiq ssenariylar
  rejected.md     — rasman rad etilgan/bekor qilingan variantlar
  dunyo/          — institutlar, geografiya, din, til (kerak bo'lsa)
  personajlar/    — har bir personaj uchun alohida fayl (kerak bo'lsa)
  variantlar/     — asar ichidagi mustaqil bo'lim/variant (masalan "5000 kishilik simulyatsiya")
  tahlil/         — adabiy/psixologik tahlil, plot-hole qaydlari
  sahnalar/       — yozilgan sahna qoralamalari (kerak bo'lsa)

_common/          — bir nechta asarga baravar tegishli g'oya banki (Lego bloklari, umumiy katalog)
_arxiv/
  xom/            — suhbat tarixi, xom matn (dalil, o'qish uchun emas)
  eksport/        — JSON eksportlar
```

**Status papka nomida emas, fayl frontmatida turadi** — chunki bitta fayl
faqat bitta papkada tura oladi, lekin Dataview kabi vositalar bilan
"barcha kanon" yoki "barcha rad etilgan" ro'yxatini chiqarish uchun
metadata kerak.

## 2. Frontmatter sxemasi

Har bir mazmunli `.md` fayl boshida:

```yaml
---
status: canon        # canon | branch | rejected | proposal | analysis | common | archive
work: soya_hukmdori   # asar slug: soya_hukmdori | abadiyat_qafasi | frederin | free_god | umumiy
updated: 2026-10-30   # YYYY-MM-DD
---
```

`status` qiymatlari:
- `canon` — tasdiqlangan, o'zgarmas asos
- `branch` — muhokama qilingan, hali tanlanmagan variant
- `rejected` — rasman rad etilgan/bekor qilingan
- `proposal` — taklif qilingan mustaqil bo'lim/variant (hali kanon emas)
- `analysis` — tashqi tahlil (kanon qismi emas, uni tushuntiradi)
- `common` — bir nechta asarga baravar tegishli
- `archive` — xom/dalil material, tahrir qilinmaydi

## 3. Nomlash

- Fayl va papka nomlari **kichik harf, pastki chiziq** (`soya_hukmdori`, `kanon.md`).
- **Bo'shliq va qavs ishlatilmaydi** — Obsidian ichki havolalarini (`[[...]]`) buzadi.
  Masalan `gemini_conversation_final (1).json` emas, `gemini_final.json`.
- Har bir asar uchun bitta `<asar_slug>` — `Asarlar/<asar_slug>/` ichida.

## 4. Chuqurlik chegarasi

3 darajadan oshmasin: `Asarlar/soya_hukmdori/variantlar/fayl.md` — OK.
`dunyo/` va `personajlar/` ichida yana papka ochmang, fayl oching
(`dunyo/geografiya.md`, `personajlar/agnes.md`).

## 5. Bitta fayl — bitta mavzu

Kanon, branch va rad etilganlarni bitta faylga aralashtirmang. Yangi g'oya
kelganda avval aniqlang: bu tasdiqlangan asos (`kanon.md`), ochiq variant
(`branch.md`) yoki rad etilgan (`rejected.md`)?

## 6. Nusxalashdan saqlaning

`_common/` dagi fayl (masalan `lego_blocks.md`) faqat bitta joyda turadi.
Asar ichida kerak bo'lsa, nusxalab ko'chirmang — `[[lego_blocks]]` havolasi
bilan chaqiring.

## 7. Xom matn arxivga

Suhbat eksportlari, to'liq turn tarixi (`turns_*`, `full_topics`, JSON
fayllar) — bular **dalil**, kundalik o'qish uchun emas. Har doim
`_arxiv/xom/` yoki `_arxiv/eksport/` ichida saqlanadi, ildizda emas.

## 8. Commit xabari

Qisqa, o'zbek tilida, nima o'zgarganini aniq yozing:

```
<asar/bo'lim>: <nima qilindi>

masalan:
soya_hukmdori: branch.md ga BRANCH L qo'shildi
_common: lego_blocks.md ga yangi blok qo'shildi
```
