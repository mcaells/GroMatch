# GroMatch: Smart Grocery Budget & Recipe Matcher

## Deskripsi Proyek
GroMatch adalah aplikasi web fullstack yang dirancang untuk menjawab permasalahan sehari-hari: "Hari ini bisa masak apa dengan uang Rp X?". Aplikasi ini membantu anak kos, mahasiswa, atau ibu rumah tangga untuk menemukan resep masakan yang sesuai dengan anggaran (budget) harian mereka, menggunakan kalkulasi harga bahan pokok yang disinkronisasi dengan data harga pasar real-time.

Proyek ini dikembangkan sebagai pemenuhan tugas individu untuk mata kuliah Rekayasa Perangkat Lunak (Semester 3), Program Studi Information Technology di Pradita University.

## Fitur Utama
- Budget-Based Recipe Matching: Pencarian resep yang difilter secara otomatis berdasarkan limitasi anggaran (Rupiah) yang diinput oleh pengguna.
- Estimated Cost Calculation: Kalkulasi estimasi harga bahan baku berdasarkan database internal harga rata-rata bahan pokok lokal (per gram/porsi).
- Auto-Generated Shopping List: Menghasilkan daftar belanja spesifik (lengkap dengan takaran) dari resep yang dipilih.
- Dietary & Ingredient Filters: Opsi untuk menyaring resep berdasarkan bahan yang sudah ada di kulkas atau alergi tertentu.

## User Flow
- Input Anggaran: Pengguna membuka aplikasi dan memasukkan budget yang dimiliki (misal: Rp 30.000) beserta target jumlah porsi.
- Kustomisasi: Pengguna memasukkan filter tambahan jika diperlukan (misal: "olahan ayam", "tanpa santan").
- Pencocokan: Sistem menarik data resep, mengkalkulasi estimasi harga setiap komponen bahan melalui database lokal, dan menampilkan 3-5 opsi masakan yang total pengeluarannya masuk dalam budget.
-  Eksekusi: Pengguna memilih salah satu resep. Aplikasi akan menampilkan instruksi memasak sekaligus checklist daftar belanja interaktif.

## Tech Stack & Tools
- Frontend: HTML, CSS, JavaScript.
- UI/UX Design: Figma.
- Backend: Python (Flask) / Java.
- Database: MySQL (Relational Schema ter-normalisasi hingga 3NF).
- Version Control: Git & GitHub.
