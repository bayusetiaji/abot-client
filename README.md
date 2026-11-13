# ABot Client

Aplikasi Flutter sederhana (Android/Web) sebagai client chatbot untuk keperluan latihan mahasiswa. Aplikasi ini mengirim pesan ke API chatbot dan menampilkan responsnya dalam tampilan chat.

## Fitur

- Tampilan chat sederhana (bubble user dan bot)
- Input pesan dan tombol kirim
- Request ke API menggunakan method `GET`
- Menampilkan respons dari server atau pesan error

## Konfigurasi API

Secara default aplikasi terhubung ke:

- **Endpoint:** `https://svc.yipsip.my.id/abot`
- **Method:** `GET`
- **Parameter:**
  - `key`: API key
  - `input`: teks pesan dari user

Konfigurasi saat ini ada di `lib/main.dart`:

```dart
static const String _apiUrl = 'https://svc.yipsip.my.id/abot';
static const String _apiKey = 'qna-st407';
```

Ubah nilai tersebut jika endpoint atau API key berbeda.

## Prasyarat

- [Flutter SDK](https://docs.flutter.dev/get-started/install) terpasang
- Perangkat/emulator Android, atau Chrome untuk menjalankan versi web

## Menjalankan Aplikasi

1. Install dependencies:
   ```bash
   flutter pub get
   ```
2. Jalankan aplikasi:
   ```bash
   flutter run
   ```

Untuk menjalankan di Chrome:

```bash
flutter run -d chrome
```

## Struktur Utama

- `lib/main.dart` — kode utama aplikasi chat client
- `pubspec.yaml` — konfigurasi dependencies Flutter
- `android/app/src/main/AndroidManifest.xml` — permission internet untuk Android

## Catatan

- Aplikasi Android memerlukan permission `INTERNET` (sudah ditambahkan).
- Jika dijalankan di web/browser, server API harus mengizinkan CORS.
