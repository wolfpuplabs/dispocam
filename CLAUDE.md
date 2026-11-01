# CLAUDE.md

## Workflow
- Selalu auto-merge: setiap perubahan dikerjakan di branch baru, dibuatkan PR ke `main`, lalu langsung di-merge (squash) tanpa perlu konfirmasi lagi.
- Setelah merge, sinkronkan `main` lokal dengan `origin/main`.

## Project
- Seluruh aplikasi ada di `index.html` (HTML + CSS + JS, tanpa build step).
- Filter film dirender oleh satu shader WebGL (`FilmRenderer`) yang dipakai untuk live preview dan capture, jadi hasil foto harus selalu sama dengan preview.
- Resep film ada di array `FILMS`; nilai default di `BASE`.
- Bahasa default UI, pesan, dan metadata adalah English.
