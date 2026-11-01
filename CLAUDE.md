# CLAUDE.md

## Workflow
- Selalu auto-merge: setiap perubahan dikerjakan di branch baru, dibuatkan PR ke `main`, lalu langsung di-merge (squash) tanpa perlu konfirmasi lagi.
- Setelah merge, sinkronkan `main` lokal dengan `origin/main`.

## Project
- Seluruh aplikasi ada di `index.html` (HTML + CSS + JS, tanpa build step).
- Filter film dirender oleh satu shader WebGL (`FilmRenderer`) yang dipakai untuk live preview dan capture, jadi hasil foto harus selalu sama dengan preview.
- Resep film ada di array `FILMS`; nilai default di `BASE`.
- Bahasa default UI, pesan, dan metadata adalah English. Ada tombol EN/ID di top bar; semua teks UI ada di objek `I18N` (tambahkan key baru ke `en` dan `id`).

## Deploy
- Vercel project `dispocam` (team Wolfpuplabs' projects) terhubung ke repo ini: setiap merge ke `main` otomatis deploy ke production, setiap branch/PR dapat preview URL. Tidak perlu deploy manual.
- Domain production: https://dispocam-by-wolfpuplabs.vercel.app/ (`dispocam-three.vercel.app` di-redirect 308 lewat `vercel.json`).
- URL absolut di meta `og:*` / `twitter:*` harus memakai domain production di atas.
