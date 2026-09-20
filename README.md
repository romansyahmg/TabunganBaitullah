# Deploy Tabungan Umroh ke Vercel

## Isi folder

- `index.html` — aplikasi utama
- `manifest.json` — konfigurasi PWA
- `sw.js` — Service Worker
- `icon-192.png` dan `icon-512.png` — ikon aplikasi

## Sebelum deploy

`index.html` sudah berisi URL Cloudflare Worker:

```javascript
const API_URL = "https://api-tabuungan-baitullah.mg-romansyah.workers.dev/";
```

Jika URL Worker berubah, ubah baris tersebut. Jangan kosongkan `API_URL`.

## Deploy lewat Vercel Dashboard

1. Upload isi folder ini ke repository GitHub.
2. Di Vercel pilih **Add New Project**.
3. Import repository tersebut.
4. Framework Preset: **Other**.
5. Build Command: kosongkan.
6. Output Directory: kosongkan.
7. Klik **Deploy**.

## Setelah deploy

Buka URL Vercel dan cek:

- `https://DOMAIN-VERCEL/`
- `https://DOMAIN-VERCEL/manifest.json`
- `https://DOMAIN-VERCEL/sw.js`

Kemudian tes login nasabah, login admin, OTP, setor, tarik, dan PWA.

Cloudflare Worker harus mengizinkan CORS dari domain Vercel yang digunakan.
