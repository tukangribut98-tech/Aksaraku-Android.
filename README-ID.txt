# Aksaraku Android — paket awal

Paket ini membungkus file HTML Aksaraku yang kamu berikan ke proyek Android berbasis Capacitor.

## Cara membangun APK dari HP Android

1. Ekstrak ZIP ini.
2. Buat akun GitHub jika belum punya, lalu buat repository baru bernama `Aksaraku-Android`.
3. Upload seluruh isi folder proyek ini ke repository (pastikan folder `.github/workflows` ikut terunggah).
4. Buka tab **Actions** di repository dan jalankan workflow **Build APK Aksaraku** melalui **Run workflow**. Jika diminta, izinkan GitHub Actions.
5. Setelah selesai, buka hasil workflow dan unduh artifact **Aksaraku-debug-apk**.
6. Ekstrak artifact ZIP, lalu instal `app-debug.apk` di HP. Android mungkin meminta izin instal aplikasi dari sumber tersebut.

## Catatan penting

- Ini adalah paket proyek awal, **belum file APK jadi**. APK dibuat oleh GitHub Actions setelah proyek diunggah.
- Workflow menghasilkan APK debug untuk instalasi pribadi, bukan APK rilis Play Store.
- ID aplikasi saat ini `com.aksaraku.app`.
- Fitur inti HTML tetap disertakan. Integrasi sidik jari Android dan penyimpanan/berbagi file native perlu tahap pengujian dan penyesuaian plugin Capacitor; jangan anggap fitur biometrik sudah aktif hanya karena proyek berhasil dibuild.
- Data aplikasi disimpan lokal di perangkat. Sebelum memasang versi baru atau menghapus aplikasi, buat cadangan terenkripsi dari menu Pengaturan Aksaraku.
- Gunakan koneksi internet saat proses build dan untuk memuat font Google yang dipakai halaman.

## Struktur

- `www/index.html` — aplikasi Aksaraku asli.
- `capacitor.config.json` — konfigurasi aplikasi.
- `package.json` — dependensi Capacitor.
- `.github/workflows/build-apk.yml` — proses build APK otomatis di GitHub Actions.
