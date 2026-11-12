[README (2).md](https://github.com/user-attachments/files/34735821/README.2.md)
# Travertin Ombor tizimi — o'rnatish yo'riqnomasi

Fayllar:
- `index.html` — butun sayt
- `schema.sql` — baza (Supabase'ga kiritiladi)
- `README.md` — shu yo'riqnoma

Hamma ma'lumot **bitta umumiy bazada** (Supabase) turadi. Omborchi yozgan narsa Nazoratda, Nazorat yozgan narsa omborchida ko'rinadi. Sayt GitHub Pages'da turadi. Hammasi bepul.

## 1. Supabase (baza)
1. https://supabase.com ga kiring va ro'yxatdan o'ting.
2. **New project**: nom `ombor`, **Database password** ni yozib qo'ying, region Frankfurt. **Create** bosing, 1–2 daqiqa kuting.
3. **Authentication → Users → Add user → Create new user**:
   - Email: `valiyevsakhobiddin@gmail.com`
   - Parol: o'zingiz o'ylagan kuchli parol (10–12 belgidan kam bo'lmasin)
   - **Auto Confirm User** ni belgilang, **Create** bosing.
4. **Authentication → Sign In / Providers → Email** → **Allow new users to sign up** ni **o'chiring** → **Save**.
5. **SQL Editor → New query** → `schema.sql` ichini to'liq tashlang → **Run**. «Success» chiqsa tayyor.
6. **Project Settings → API** dan nusxalang:
   - **Project URL**
   - **anon public** kalit (`eyJ...`)

   **service_role** kalitni hech qayerga qo'ymang.

## 2. index.html ni sozlash
`index.html` ni Notepad bilan oching, yuqoridagi ikki qatorni to'ldiring:
```js
const SUPABASE_URL = 'https://xxxx.supabase.co';
const SUPABASE_KEY = 'eyJ...';
```
Saqlang.

## 3. GitHub Pages (saytni internetga chiqarish)
1. https://github.com da ro'yxatdan o'ting.
2. **+ → New repository**: nom `ombor`, **Public**, **Create repository**.
3. **uploading an existing file** → `index.html` ni tashlang → **Commit changes**.
4. **Settings → Pages** → Source: **Deploy from a branch** → Branch: `main` / `(root)` → **Save**.
5. 1–2 daqiqadan so'ng havola chiqadi: `https://LOGININGIZ.github.io/ombor/`

## 4. Ishlatish
**Nazorat** (siz): email va parol bilan kirasiz.
- **Mahsulotlar** — Excel'dan yuklash (ustunlar: `Nomi | Miqdor | Birlik`, «Excel namuna» tugmasi namunani beradi) yoki qo'lda qo'shish, tahrirlash, o'chirish.
- **Omborchilar** — ism qo'shasiz, kod avtomatik chiqadi, «Mahsulotlar» tugmasi bilan unga mahsulot biriktirasiz. Kodni almashtirish va o'chirib qo'yish ham mumkin.
- **Tarix** — kim, qachon, nimani, qanchadan qanchaga o'zgartirgani. Excel'ga yuklab olinadi.
- **Hisobot** — kunlik, oylik yoki oraliq. Omborchilar bo'yicha jadval, mahsulotlar bo'yicha boshida/kirim/chiqim/oxirida, bitta omborchini tanlab uning alohida hisoboti. Excel'ga yuklash va chop etish bor.

**Omborchi**: saytni ochadi, **Omborchi** bo'limiga kodni kiritadi, ismi chiqadi, faqat o'ziga biriktirilgan mahsulotlarni ko'radi:
- **Kirim** — mahsulot keldi, qo'shiladi
- **Chiqim** — ishlab chiqarishga ketdi, ayriladi (omborda yetmasa ruxsat bermaydi)
- **Haqiqiy qoldiq** — sanab ko'rilgan miqdor (masalan 1000 → 950)
- Har bir amalda omborchining ismi va vaqti yoziladi.

## Ma'lumot ikki tomonga qanday ko'rinadi
- Omborchi o'zgartirsa, sizda **Mahsulotlar**, **Tarix** va **Hisobot** da ismi bilan chiqadi (sizning sahifangizda yangilash uchun F5 bosing yoki tabni qayta oching).
- Siz o'zgartirsangiz, omborchida 30 soniya ichida o'zi yangilanadi yoki «Yangilash» tugmasi bilan darhol ko'rinadi.

## Xavfsizlik
- Jadvallarga faqat siz (admin) to'g'ridan-to'g'ri kira olasiz. Omborchilar faqat kod orqali ishlaydigan maxsus funksiyalardan foydalanadi va faqat o'z mahsulotlariga tegadi.
- Kodlar 8 belgili tasodifiy. Omborchi ishdan ketsa — «O'chirish» yoki «Yangi kod».
- Parolni omborchilarga bermang, ularga faqat kod bering.

## Keyinroq o'zgartirish
`index.html` ni o'zgartirsangiz, GitHub'da **Add file → Upload files** orqali qaytadan yuklang (bir xil nom, ustiga yoziladi).

## Muammolar
- **«Sozlanmagan» yozuvi chiqsa:** 2-qadamdagi URL va kalit to'ldirilmagan.
- **Nazoratga kira olmasam:** email va parol Supabase Users dagi bilan bir xilmi, va `schema.sql` dagi admin email ham shumi tekshiring.
- **Bepul tarifda** loyiha 1 hafta ishlatilmasa to'xtab qolishi mumkin; Supabase'ga kirib «Restore» bosing. Muhim ma'lumotdan vaqti-vaqti bilan Tarixdan Excel nusxa oling.
