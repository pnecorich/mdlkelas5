# Belajar Seru (Kelas 5 SD)

## Pasang pertama kali (sekali saja)
1. Buat repo di GitHub (mis. `belajar-sd`), upload **semua isi folder ini** ke root repo.
2. Repo → Settings → Pages → Source: branch `main`, folder `/ (root)`.
3. Buat token: GitHub → Settings → Developer settings → Fine-grained tokens → pilih repo itu saja → izin **Contents: Read and write**.
4. Buka `https://USERNAME.github.io/belajar-sd/admin.html`, masuk dengan password, isi username, nama repo, dan token, klik Simpan.

## Tambah chapter baru
1. Minta chapter baru ke Claude (kirim foto tabel materi). Hasilnya satu file JSON.
2. Nama file harus: `g<kelas>-<pelajaran>-ch<nomor 2 digit>.json`, contoh `g5-english-ch07.json`.
3. Buka admin → pilih file → Upload. Tunggu 1–2 menit, chapter muncul di landing page.

Jika nama file tidak cocok dengan isi `meta` di dalam file, panel menolak dan menjelaskan alasannya.

## Format JSON (ringkas)
- `meta`: grade, subject (huruf kecil, tanpa spasi), subjectName, subjectEmoji, chapter, title, emoji
- `pages`: type `vocab` (items: e, en, id), `explain` (intro, blocks), `story` (lines: en, id)
- `quiz`: 20 soal, level `medium` (15) atau `hard` (5, wajib ada `hint`), `options` + `answer` (indeks mulai 0), `explain`
- Teks boleh pakai `**tebal**` dan `\n` untuk baris baru.
