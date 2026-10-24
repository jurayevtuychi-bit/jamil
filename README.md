# AI Teach Edu — Android ilovasi

https://www.ai-teach-edu.uz/ saytini ilova ichida ochadigan WebView ilovasi.

Imkoniyatlar: yuklanish chizig'i, "orqaga" tugmasi bilan sahifalar bo'ylab qaytish, internet yo'q bo'lganda "Qayta urinish" ekrani, YouTube va boshqa videolar uchun to'liq ekran rejimi, sayt tashqarisidagi havolalarni telefon brauzerida ochish, PDF/DOCX yuklab olish havolalarini tashqi ilovada ochish.

## APK olish — 1-usul: GitHub orqali (kompyuterga hech narsa o'rnatmasdan)

1. github.com da bepul akkaunt oching va yangi repozitoriy yarating.
2. Shu papkadagi barcha fayllarni (`.github` papkasi bilan birga) repozitoriyga yuklang.
3. Repozitoriyda **Actions** bo'limiga kiring. "Build APK" jarayoni o'zi ishga tushadi (3–6 daqiqa). Ishga tushmasa, **Run workflow** tugmasini bosing.
4. Tugagach, jarayon sahifasining pastidagi **Artifacts** bo'limidan `ai-teach-edu-apk` ni yuklab oling. Ichida `app-debug.apk` bor.

## APK olish — 2-usul: Android Studio

1. Android Studio'ni o'rnating va **Open** orqali shu papkani oching. Gradle sinxronlanishini kuting.
2. **Build → Build Bundle(s) / APK(s) → Build APK(s)** ni tanlang.
3. APK `app/build/outputs/apk/debug/app-debug.apk` manzilida bo'ladi.

## Telefonga o'rnatish

`app-debug.apk` ni telefonga yuboring, ochganda "noma'lum manbalardan o'rnatishga ruxsat" so'ralsa, ruxsat bering. Talab: Android 8.0 va undan yuqori.

## Sozlash

- Sayt manzili: `MainActivity.java` ichidagi `HOME_URL`.
- Ilova ichida ochiladigan domenlar: shu fayldagi `INTERNAL_HOSTS`. Boshqa domenlar brauzerda ochiladi.
- Ilova nomi: `app/src/main/res/values/strings.xml`. Asosiy rang: `colors.xml`.
- Ikonka: `res/drawable/ic_launcher_foreground.xml` (o'zingizning logotipingizni Android Studio'da **File → New → Image Asset** orqali qo'yishingiz mumkin).

## Google Play uchun

`app-debug.apk` o'rnatish va tarqatish uchun yaraydi, lekin Google Play'ga yuklash uchun o'z kalitingiz bilan imzolangan release (AAB) kerak bo'ladi. Kalitni (`.jks`) hech qachon ochiq repozitoriyga qo'ymang.
