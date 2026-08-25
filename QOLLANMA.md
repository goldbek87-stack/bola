# "Bilim va Mukofot" — APK olish qo'llanmasi

Kompyuteringizga hech narsa o'rnatmasdan, GitHub'ning bepul bulut xizmati orqali
tayyor APK faylini olasiz. HTML dasturingizga hech qanday o'zgartirish
kiritilmagan — u aynan `www/index.html` faylida turibdi.

## 1-qadam: GitHub akkaunt oching
1. https://github.com ga kiring
2. "Sign up" tugmasi orqali bepul akkaunt yarating (agar bo'lmasa)

## 2-qadam: Yangi repository (loyiha) yarating
1. GitHub'da yuqori o'ngdagi **+** belgisini bosing → **New repository**
2. Nomi: masalan `bilim-va-mukofot`
3. **Public** qilib qoldiring (bepul Actions uchun qulay)
4. **Create repository** tugmasini bosing

## 3-qadam: Fayllarni yuklang
1. Ochilgan repository sahifasida **"uploading an existing file"**
   (yoki "Add file" → "Upload files") havolasini bosing
2. Sizga berilgan zip fayldagi **barcha papka va fayllarni** shu joyga
   tashlang (drag-and-drop qiling). Muhim: papka tuzilishi saqlanishi kerak:
   ```
   config.xml
   package.json
   www/index.html
   .github/workflows/build-apk.yml
   ```
   Agar GitHub veb-interfeysi `.github` papkasini alohida yuklashda
   qiynasa, uni alohida "Add file → Create new file" orqali
   `.github/workflows/build-apk.yml` nomi bilan yaratib, ichiga shu
   faylning matnini joylashtiring.
3. Pastda **Commit changes** tugmasini bosing

## 4-qadam: Qurilish (build) jarayonini ishga tushiring
1. Repository sahifasida yuqoridagi **Actions** bo'limiga o'ting
2. "Build Android APK" workflow'ini tanlang
3. Agar avtomatik boshlanmagan bo'lsa, **Run workflow** tugmasini bosing
4. 3-6 daqiqa kutib turing (yashil ✅ belgisi chiqguncha)

## 5-qadam: Tayyor APK-ni yuklab oling
1. Tugagan workflow ustiga bosing
2. Pastdagi **Artifacts** qismida **bilim-va-mukofot-apk** deb yozilgan
   faylni bosib yuklab oling (bu — zip ichida APK)
3. Zipni oching, ichidan `app-debug.apk` faylini telefoningizga o'tkazing
   va o'rnating (Android sozlamalarida "Noma'lum manbalardan o'rnatish"ga
   ruxsat berish kerak bo'lishi mumkin)

## Eslatma
- Bu — **debug APK**, ya'ni sinov/shaxsiy foydalanish uchun ishlaydi.
  Agar Google Play'ga chiqarish kerak bo'lsa, keyinchalik "release" (imzolangan)
  versiya kerak bo'ladi — bu alohida qadam.
- HTML dasturingiz ichidagi funksiyalarga (JavaScript kod, dizayn va h.k.)
  hech narsa tegilmadi. Faqat uni Android ilova qobig'iga (Cordova) o'rab
  qo'ydik.
- Agar Actions bepul limitidan chiqib qolsangiz (juda ehtimoli past,
  chunki public repo'larda GitHub Actions bepul), xatolik xabari chiqadi —
  shunda menga yozing, boshqa yo'l (masalan PWABuilder.com) taklif qilaman.
