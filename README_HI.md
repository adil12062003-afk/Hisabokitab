# Mera Hisab Pro — Android APK project

Yeh project tumhare updated HTML app ko Android WebView app ke andar chalata hai. App ka hisaab aur custom UPI app list device ke local browser storage mein rehte hain.

## GitHub se APK banane ka sabse aasan tareeqa

1. ZIP ko extract karo.
2. GitHub par naya repository banao, jaise `Mera-Hisab-Pro`.
3. Extract kiye hue **folder ke andar ke saare files** repository ke root mein upload karo. `.github/workflows/build-apk.yml` bhi upload hona chahiye.
4. GitHub mein **Actions** tab kholo.
5. `Build Mera Hisab Pro APK` workflow select karke **Run workflow** dabao. `main`/`master` par push karne se bhi build automatic start hota hai.
6. Green tick aane par workflow run kholo, neeche **Artifacts** mein `Mera-Hisab-Pro-debug-APK` download karo.
7. Artifact ZIP extract karo. Uske andar `app-debug.apk` hoga. Phone par install karne ke liye Android tumse unknown source installation allow karne ko keh sakta hai.

## Android Studio se

Android Studio mein extracted project folder kholo. JDK 17 aur Android SDK Platform 35 install/available hon. Gradle sync ke baad **Build > Build APK(s)** chalao. APK yahan milega: `app/build/outputs/apk/debug/app-debug.apk`.

## Zaroori baatein

- Yeh **debug APK** hai, Play Store release/signed production APK nahi.
- App data phone ke app storage mein save hota hai. App uninstall ya app data clear karne par data mit sakta hai, isliye Backup tab se JSON backup nikaalte raho.
- Backup export app ke file-save picker se JSON file save karta hai; import picker se JSON backup choose karo.
- APK ko pehle test karo. Agar koi issue aaye to screenshot aur exact step bhejo.
