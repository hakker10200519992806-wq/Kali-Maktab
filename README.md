# Kali Maktab — APK qurish

## Eng oson yo'l: GitHub (kompyuter kerak emas, Android Studio kerak emas)
1. github.com da bepul akkaunt oching, yangi **private** repozitoriy yarating.
2. Shu papkadagi hamma narsani yuklang (**Add file > Upload files**).
3. Agar `.github` papkasi yuklanmasa: **Add file > Create new file**, nomiga `.github/workflows/apk.yml` yozing va `github-workflow-apk.yml` ichidagi matnni joylang.
4. **Actions** bo'limiga kiring, "APK qurish" tugagach (~5-8 daqiqa), pastdagi **KaliMaktab-apk** artefaktini yuklab oling (zip ichida `app-debug.apk`).
5. APK ni telefonga o'tkazing, "noma'lum manbalardan o'rnatish"ga ruxsat bering va o'rnating.

## Kompyuterda (Node 18+, JDK 17, Android SDK)
npm install && npx cap add android && npx cap sync android
cd android && ./gradlew assembleDebug
APK: android/app/build/outputs/apk/debug/app-debug.apk

## Ilovani yangilash
`www/` ichidagi fayllarni almashtiring va qayta quring. Har yangilanishda `www/sw.js` dagi `kms-vN` raqamini oshiring.
