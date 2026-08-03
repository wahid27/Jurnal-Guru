JURNAL MENGAJAR DIGITAL — PWA PRODUCTION

TUJUAN
Paket ini membuat Web App Google Apps Script tampil dan dapat dipasang
seperti aplikasi Android melalui Chrome.

ARSITEKTUR
PWA Wrapper → Google Apps Script Web App → Spreadsheet + Google Drive + PDF

INSTALASI
1. Upload seluruh folder ke hosting HTTPS.
2. Buka index.html.
3. Cari CONFIG.GAS_URL.
4. Ganti:
   PASTE_URL_WEB_APP_GAS_DI_SINI
   dengan URL deployment Web App Apps Script Anda.
5. Upload/simpan kembali.
6. Buka alamat PWA menggunakan Chrome Android.
7. Gunakan tombol "Install Aplikasi" jika muncul, atau menu Chrome:
   "Tambahkan ke layar utama / Install app".

PENTING
- Hosting PWA harus HTTPS.
- Jangan menaruh ID Spreadsheet, password, token, atau data rahasia di index.html.
- Data jurnal tidak dicache oleh service worker.
- Google Apps Script tetap menjadi backend dan sumber data.
- Jika ingin memaksa pembaruan wrapper, ubah CACHE_NAME di sw.js dari v1 ke v2.

KUSTOMISASI
Identitas utama ada di CONFIG pada index.html:
GAS_URL     = URL Web App GAS
APP_NAME    = nama aplikasi
SCHOOL_NAME = nama sekolah

Untuk mengganti logo, ganti icon-192.svg dan icon-512.svg dengan ikon milik sekolah.
