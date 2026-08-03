# Jurnal Mengajar Digital — PWA v2

## Deploy ke GitHub Pages

1. Upload seluruh isi folder ini ke repository GitHub.
2. Pastikan `index.html` berada di root repository.
3. Buka **Settings → Pages**.
4. Source: **Deploy from a branch**.
5. Branch: `main`, folder: `/ (root)`.
6. Simpan dan tunggu GitHub Pages aktif.
7. Buka URL HTTPS Pages dari Chrome Android.

## Hubungkan ke Google Apps Script

Buka `index.html`, cari:

```js
const CONFIG = Object.freeze({
  GAS_URL: "PASTE_URL_WEB_APP_GAS_DI_SINI",
  APP_NAME: "Jurnal Mengajar Digital",
  SCHOOL_NAME: "MTs Al Istiqomah"
});
```

Ganti `GAS_URL` dengan URL **Web App GAS yang berakhiran `/exec`**.

Contoh:
`https://script.google.com/macros/s/ID_DEPLOYMENT/exec`

## Catatan

- PWA ini adalah wrapper; database, jurnal, PDF, dan Drive tetap dikelola oleh GAS.
- Service Worker tidak mencegat request ke Google Apps Script.
- HTTPS diperlukan agar install PWA dan Service Worker berjalan normal.
- Untuk nama sekolah/branding, ubah `SCHOOL_NAME` dan judul jika diperlukan.
