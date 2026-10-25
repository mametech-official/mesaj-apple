# 🍎 Mesaj — Apple iOS (App Store) Resmi Deposu

Bu depo, **Mesaj — Yeni Nesil Anlık İletişim** uygulamasının **Apple App Store (iPhone & iPad)** için hazırlanmış yerel **Capacitor + Xcode (`ios/App/App.xcodeproj`)** projesidir.

- **Paket Kimliği (Bundle Identifier):** `com.mametech.mesaj`
- **Uygulama Adı:** `Mesaj`
- **Hazır Apple İzin Açıklamaları (`ios/App/App/Info.plist`):**
  - 📷 `NSCameraUsageDescription` — Görüntülü görüşme ve fotoğraf/video çekimi
  - 🎙️ `NSMicrophoneUsageDescription` — Sesli/görüntülü görüşme ve sesli mesaj
  - 📍 `NSLocationWhenInUseUsageDescription` — Canlı harita ve konum paylaşımı
  - 🖼️ `NSPhotoLibraryUsageDescription` — Fotoğraf ve video paylaşımı
  - 🔒 `ITSAppUsesNonExemptEncryption = false` — App Store Connect dışa aktarım uyumluluğu hazır

---

## 🚀 1. Otomatik macOS Bulut Derlemesi ve `.IPA` İndirme (GitHub Actions)

Mac bilgisayarınız olmasa bile, bu depoya yapılan her güncellemede **GitHub Actions (`macos-latest`)** bulut sunucusu üzerinde Xcode projesini otomatik olarak derler ve `.ipa` paketini üretir:

1. Bu deponun üst menüsünden **[Actions](../../actions)** sekmesine tıklayın.
2. En üstteki **Apple iOS (Xcode & IPA) Build** çalışmasına tıklayın.
3. Sayfanın altındaki **Artifacts** bölümünden **`Mesaj-Apple-iOS-Paketi`** (`Mesaj-iOS-Unsigned.ipa`) dosyasını indirin.

---

## 🛠️ 2. Xcode ile Apple App Store Connect'e Gönderme

Uygulamayı Apple Developer hesabınızla imzalayıp **App Store Connect / TestFlight**'a yüklemek için:

```bash
git clone https://github.com/mametech-official/mesaj-apple.git
cd mesaj-apple
npm install
npx cap sync ios
npx cap open ios
```

1. Açılan **Xcode** ekranında sol panelden **App** projesini seçin.
2. **Signing & Capabilities** sekmesinden **Team** olarak kendi Apple Developer hesabınızı seçin.
3. Üst menüden **Product > Archive** seçeneğine tıklayıp **Distribute App > App Store Connect** adımlarını izleyin.

---

## 🔗 Diğer Platform Depoları
- 🌐 **Web (PWA) Deposu:** [mametech-official/mesaj](https://github.com/mametech-official/mesaj)
- 🤖 **Android (Google Play Store) Deposu:** [mametech-official/mesaj-android](https://github.com/mametech-official/mesaj-android)
