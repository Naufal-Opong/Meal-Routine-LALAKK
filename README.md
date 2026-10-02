# Meal Routine Lalakk ♡

Aplikasi web/PWA sederhana untuk membantu membangun rutinitas makan yang lebih teratur.

## Fitur

- UI pastel pink + kelinci
- Onboarding
- Jadwal makan yang dapat disesuaikan
- Progress harian
- Countdown ke jadwal berikutnya
- Tandai sudah makan
- Penundaan +10 menit
- Status izin notifikasi
- PWA manifest
- Service worker untuk cache/offline dasar
- Siap di-host sebagai static site

## Struktur

```text
meal-routine/
├── index.html
├── manifest.json
├── sw.js
├── .nojekyll
└── icons/
    ├── icon-192.svg
    └── icon-512.svg
```

## Deploy dengan GitHub Pages

1. Buat repository baru di GitHub.
2. Upload seluruh isi folder ini, bukan file ZIP-nya.
3. Buka **Settings → Pages**.
4. Pilih **Deploy from a branch**.
5. Pilih branch utama dan folder `/ (root)`.
6. Simpan dan tunggu GitHub Pages selesai melakukan deploy.
7. Buka URL Pages melalui HTTPS.
8. Di HP, buka URL tersebut lalu gunakan **Add to Home Screen / Install app** jika tersedia.

## Catatan notifikasi

Browser notification membutuhkan izin pengguna dan konteks yang aman (HTTPS saat online).
JavaScript halaman dapat memunculkan reminder ketika halaman aktif. PWA/service worker membantu instalasi dan caching, tetapi service worker saja bukan scheduler alarm yang menjamin notifikasi terjadwal saat browser benar-benar tidak aktif.

Untuk reminder yang benar-benar reliable di background, tahap berikutnya adalah membuat mekanisme notifikasi native/Push atau Android app.
