# GroMatch: Smart Grocery Budget & Recipe Matcher

## Masalah Nyata yang Akan Diselesaikan
Banyak orang, terutama anak kos dan ibu rumah tangga, sering kebingungan menentukan menu masakan harian yang pas dengan sisa uang di dompet. Tanpa perencanaan, mereka sering kali membeli bahan makanan secara impulsif yang berujung pada pengeluaran overbudget atau makanan yang terbuang (food waste). Belum ada aplikasi pencari resep yang secara otomatis menyaring hasil masakannya berdasarkan batasan Rupiah yang dimiliki pengguna secara realistis.

## Profil Target Pengguna
- Mahasiswa / Anak Kos: Memiliki anggaran makan harian atau mingguan yang sangat ketat dan butuh resep praktis.
- Ibu Rumah Tangga Muda: Membutuhkan variasi menu keluarga tanpa melebihi uang belanja bulanan.
- Pekerja Entry-Level: Ingin berhemat dengan membawa bekal masak sendiri dari rumah, namun tidak punya banyak waktu untuk riset harga bahan di pasar.

## Manfaat Aplikasi
- Efisiensi Finansial: Mencegah pengeluaran overbudget karena pengguna hanya melihat resep yang mampu mereka beli.
- Menghemat Waktu: Menghilangkan kebingungan "hari ini masak apa ya?" dengan memberikan rekomendasi instan beserta takaran bahannya.
- Manajemen Belanja Terstruktur: Menghasilkan daftar belanja (shopping list) otomatis yang mempermudah proses belanja di pasar atau supermarket.

## Daftar Fitur Inti
- Budget & Portion Input: Formulir bagi pengguna untuk memasukkan maksimal anggaran (dalam Rupiah) dan jumlah porsi yang diinginkan.
- Recipe Matching Engine: Mesin pencari yang mengkalkulasi harga bahan baku dari database harga rata-rata lokal dan membandingkannya dengan resep dari Spoonacular API.
- Dietary Filters: Fitur penyaring resep berdasarkan preferensi atau alergi (misal: "tanpa kacang", "olahan ayam").
- Auto-Shopping List: Generator daftar belanja interaktif berdasarkan resep yang dipilih.
- User Management (CRUD): Fitur pendaftaran akun, login, dan kemampuan menyimpan (save/bookmark) resep favorit ke dalam profil pengguna (menggunakan database MySQL).

## Fitur yang Tidak Dikerjakan (Out of Scope)
- Integrasi Harga Pasar Real-Time: Aplikasi tidak akan menarik data harga secara real-time dari API pemerintah karena kendala stabilitas server publik. Harga yang digunakan adalah harga estimasi rata-rata yang disimpan secara statis di database internal.
- E-Commerce / Delivery Bahan Makanan: Aplikasi murni berfungsi sebagai perencana belanja dan resep. Tidak ada fitur pemesanan atau pengantaran bahan makanan via kurir (seperti integrasi GoMart/GrabMart).
- Payment Gateway: Tidak ada sistem transaksi keuangan di dalam aplikasi.

## Kriteria Aplikasi Dinyatakan Berhasil
- Aplikasi berhasil memfilter dan menampilkan minimal 3 rekomendasi resep yang total estimasi harga bahannya tidak melebihi budget yang diinput pengguna.
- Kalkulasi harga berjalan logis: Sistem berhasil mengonversi takaran bahan dari API (misal: 100 gram bawang) dikalikan dengan data harga di MySQL, lalu menampilkan total estimasinya ke layar.
- Fungsi integrasi API eksternal berjalan baik: Dapat menarik gambar, instruksi memasak, dan komposisi dari Spoonacular API tanpa error.
- Fungsi Database berjalan baik: Pengguna dapat membuat akun, menyimpan resep, dan melihat kembali daftar resep favorit mereka saat melakukan login ulang.

## Tech Stack & Tools
- Frontend: HTML, CSS, JavaScript (Fetch API)
- Backend: Python (Flask) / Java
- Database: MySQL (Relational Schema hingga 3NF)
- External API: Spoonacular API
