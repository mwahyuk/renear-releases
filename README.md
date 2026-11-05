# Renear: unduhan

Renear adalah aplikasi desktop Windows untuk merekam rapat, mentranskrip audio, dan menyusun MoM (notulen) atau laporan ke Word dan PDF memakai template kantor.

## Fitur utama

- **Rekam rapat:** mikrofon, suara sistem (Zoom, Meet, Teams), atau keduanya. Mic dan suara sistem bisa dibisukan sendiri-sendiri, dan gain mikrofon bisa diatur.
  - Dua rapat yang berjalan bersamaan juga bisa direkam terpisah, asalkan suaranya diputar ke perangkat berbeda. Contoh: satu rapat ke speaker, satu lagi ke headset.
  - Rekaman yang sudah ada (WAV, MP3, M4A, FLAC, OGG) bisa diimpor.
- **Transkrip otomatis** setiap ±10 menit selama rapat berlangsung. Bahasa dikenali otomatis.
- **Dokumentasi:**
  - screenshot window rapat secara berkala;
  - tombol **Snap** untuk screenshot kapan saja;
  - foto yang diunggah sendiri, misalnya foto ruang rapat.
- **MoM dan laporan** disusun AI dari transkrip, lalu bisa disunting sebelum diekspor ke Word atau PDF dengan template kantor. Ada pratinjau halaman seperti di Word.
- **Backup dan pindah perangkat:** semua rapat, dokumen, dan pengaturan disimpan ke satu file, lalu bisa diimpor di komputer lain.
- **Mode terang/gelap** dan **update otomatis** di latar belakang.

## Cara memasang

1. Buka halaman [Releases](https://github.com/mwahyuk/renear-releases/releases/latest) dan unduh `Renear_<versi>_x64-setup.exe`.
2. Jalankan installer. Bila muncul **"Windows protected your PC"**, klik **More info → Run anyway**. Installer belum memakai sertifikat code signing.
3. Buka Renear dan mulai rekam. Transkripsi dan pembuatan MoM langsung bisa dipakai tanpa mengisi API key apa pun, dengan kuota pemakaian bulanan.

### Memakai API key sendiri (opsional)

Kalau ingin memakai akun AI sendiri, buka **Pengaturan → AI & API**, aktifkan **Pakai API key sendiri**, lalu tambahkan key:

- **Groq** (transkripsi): gratis di console.groq.com.
- **Google Gemini** (MoM dan laporan): gratis di aistudio.google.com.

Tombol **Dapatkan key** di Renear langsung membuka halaman pembuatannya. Dengan key sendiri, pemakaian mengikuti batas akun Anda.

### Ekspor PDF

Ekspor PDF memakai **Microsoft Word**, **LibreOffice**, atau **GenOffice**, mana pun yang terpasang. Ekspor Word bisa dipakai tanpa ketiganya.

## Update

Renear mengecek versi baru saat dibuka dan beberapa kali sehari. Versi baru diunduh di latar belakang dan dipasang saat Renear ditutup, tidak saat rekaman berjalan. Pengaturannya ada di **Pengaturan → Aplikasi**.

## Data dan privasi

- Rekaman, transkrip, dokumen, dan pengaturan tersimpan di komputer Anda (`%APPDATA%\com.renear.app`). API key disimpan di Windows Credential Manager.
- Untuk transkripsi dan pembuatan dokumen, audio dan teks rapat dikirim ke layanan AI pihak ketiga (Groq, Google Gemini, Agnes AI), baik lewat layanan Renear maupun langsung bila memakai key sendiri. Isi rapat tidak disimpan oleh layanan Renear.
- Untuk rapat yang bersifat rahasia, sebaiknya tidak memakai fitur AI.

## Riwayat perubahan

Catatan setiap versi ada di halaman [Releases](https://github.com/mwahyuk/renear-releases/releases). Di dalam aplikasi, riwayat versi bisa dibuka di **Pengaturan → Aplikasi**.

Repo ini hanya berisi file rilis; kode sumber Renear tidak dipublikasikan.
