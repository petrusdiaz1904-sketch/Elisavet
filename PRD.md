# PRODUCT REQUIREMENTS DOCUMENT (PRD)

## Website Klinik Veteriner dan Sistem Kasir

**Versi:** 1.0
**Status:** Draf kebutuhan produk
**Platform:** Web responsif
**Teknologi:** Laravel, Laravel Herd, SQLite
**Target pengguna:** Admin/pemilik klinik dan petugas kasir

---

## 1. MASALAH

### 1.1 Latar Belakang

Klinik veteriner membutuhkan sistem yang dapat mengelola informasi klinik sekaligus mendukung kegiatan operasional sehari-hari, seperti pendaftaran pasien hewan, penjualan obat, pencatatan layanan, pembayaran, dan pembuatan nota.

Apabila kegiatan tersebut dilakukan secara manual atau menggunakan aplikasi yang terpisah, beberapa masalah dapat muncul, seperti kesulitan mencari data pasien, ketidaksesuaian stok obat, kesalahan perhitungan pembayaran, dan kesulitan menyusun laporan pendapatan serta laba.

Klinik juga membutuhkan website publik sebagai sarana informasi bagi masyarakat mengenai profil klinik, dokter hewan, layanan, harga, obat, dan edukasi kesehatan hewan.

### 1.2 Permasalahan yang Ingin Diselesaikan

1. Belum tersedianya pusat informasi klinik yang dapat diakses masyarakat secara online.
2. Pencatatan data pasien hewan dan riwayat pemeriksaan perlu dilakukan secara terstruktur.
3. Pengelolaan obat, harga jual, harga modal, dan stok membutuhkan pencatatan yang terintegrasi.
4. Proses transaksi kasir perlu menghitung biaya obat, layanan, diskon, dan biaya tambahan secara otomatis.
5. Pembuatan nota pembayaran perlu dilakukan secara praktis melalui PDF.
6. Pemilik klinik membutuhkan laporan transaksi, pendapatan, penjualan obat, stok, layanan, dan laba.
7. Perubahan atau pembatalan transaksi perlu tercatat agar dapat ditelusuri.
8. Pengelolaan konten website harus dapat dilakukan tanpa mengedit kode program.

### 1.3 Tujuan Produk

Membangun satu aplikasi web terintegrasi yang menggabungkan website publik klinik veteriner dan sistem manajemen operasional klinik, khususnya kasir, pasien, obat, layanan, transaksi, nota, dan laporan.

---

## 2. PENGGUNA

### 2.1 Admin/Pemilik Klinik

Admin merupakan pengguna dengan hak akses penuh.

Kebutuhan:

- Mengelola akun dan hak akses pengguna.
- Mengelola data pasien hewan dan riwayat pemeriksaan.
- Mengelola data obat, harga modal, harga jual, serta stok.
- Mengelola daftar layanan dan harga.
- Mengelola transaksi dan pembatalan.
- Melihat riwayat perubahan transaksi.
- Mengakses seluruh laporan operasional dan keuangan.
- Mengelola konten website publik.
- Mengatur informasi klinik dan logo untuk nota.
- Memantau stok minimum serta melakukan penyesuaian persediaan.

### 2.2 Petugas Kasir

Kasir merupakan pengguna dengan akses terbatas sesuai tugas operasional.

Kebutuhan:

- Login ke sistem.
- Mencari dan mendaftarkan pasien hewan.
- Memilih pasien secara opsional ketika membuat transaksi.
- Memilih obat dan layanan dari daftar yang tersedia.
- Memasukkan jumlah obat atau layanan.
- Melihat harga dan total tagihan.
- Memasukkan diskon atau biaya tambahan jika diperlukan.
- Mencatat metode pembayaran.
- Menyelesaikan transaksi setelah pembayaran lunas.
- Mengunduh atau mencetak nota PDF.
- Mencari transaksi terdahulu dan mengunduh ulang nota.
- Mengubah atau membatalkan transaksi sesuai izin sistem, dengan seluruh perubahan tercatat.

### 2.3 Pengunjung Website

Pengunjung merupakan masyarakat yang mengakses website tanpa harus memiliki akun.

Kebutuhan:

- Melihat profil klinik dan informasi kontak.
- Melihat profil dokter hewan.
- Melihat daftar layanan beserta harga.
- Melihat informasi obat yang dipublikasikan.
- Membaca artikel kesehatan hewan.
- Melihat lokasi dan jam operasional klinik.
- Menghubungi klinik melalui WhatsApp.
- Mengajukan reservasi dengan diarahkan ke WhatsApp klinik.

---

## 3. FITUR

### 3.1 Website Publik

Website publik menyediakan halaman berikut:

1. **Beranda:** menampilkan ringkasan klinik, informasi utama, dan layanan unggulan.
2. **Profil Klinik:** menampilkan profil, sejarah, visi, misi, dan informasi klinik.
3. **Layanan dan Harga:** menampilkan jenis layanan serta harga yang ditetapkan.
4. **Informasi Obat:** menampilkan informasi obat atau produk yang dipilih untuk dipublikasikan.
5. **Profil Dokter Hewan:** menampilkan nama, foto, dan informasi profesional dokter.
6. **Artikel Kesehatan Hewan:** menampilkan artikel edukasi dan perawatan hewan.
7. **Kontak dan Lokasi:** menampilkan alamat, nomor kontak, WhatsApp, peta, dan jam operasional.
8. **Reservasi Online:** menyediakan tombol untuk membuka WhatsApp klinik dengan pesan awal yang dapat diisi otomatis.

Seluruh halaman harus responsif dan dapat digunakan melalui komputer, laptop, maupun ponsel.

### 3.2 Autentikasi dan Hak Akses

Sistem menyediakan login untuk admin dan kasir.

- Admin memiliki akses penuh.
- Kasir hanya dapat mengakses fungsi operasional yang diizinkan.
- Pengunjung website tidak membutuhkan login.
- Hak akses diperiksa pada sisi server, bukan hanya dengan menyembunyikan tombol pada antarmuka.
- Akun pengguna dapat dikelola oleh admin.

### 3.3 Manajemen Pasien Hewan

Sistem menyediakan fitur untuk menambah, melihat, mencari, memperbarui, dan mengarsipkan pasien.

Data pasien meliputi:

- Nama hewan.
- Jenis hewan.
- Ras.
- Umur atau tanggal lahir.
- Jenis kelamin.
- Berat badan.
- Nama pemilik.
- Nomor telepon pemilik.
- Riwayat pemeriksaan atau penyakit.
- Keterangan tambahan berupa teks bebas.

Pasien dapat dicari berdasarkan informasi yang relevan, seperti nama hewan atau nama pemilik.

Riwayat pemeriksaan dapat dicatat dan ditampilkan secara kronologis. Data pasien yang diarsipkan tetap dapat dirujuk untuk melihat riwayat sebelumnya.

### 3.4 Manajemen Obat dan Persediaan

Sistem menyediakan pengelolaan master obat yang meliputi:

- Nama obat.
- Kategori atau jenis obat.
- Harga modal.
- Harga jual.
- Jumlah stok.
- Batas minimum stok.
- Satuan obat.
- Keterangan tambahan bila diperlukan.

Fungsi persediaan:

- Mencatat stok masuk.
- Mencatat stok keluar.
- Melakukan penyesuaian stok dengan alasan yang tercatat.
- Menampilkan riwayat pergerakan stok.
- Memberikan indikator ketika stok mencapai atau berada di bawah batas minimum.
- Mengurangi stok secara otomatis ketika transaksi selesai.
- Mengembalikan stok yang relevan ketika transaksi penjualan dibatalkan secara sah.
- Mencegah penjualan melebihi stok tersedia.

Obat yang sudah digunakan dalam transaksi tidak boleh dihapus secara permanen. Obat tersebut dapat dinonaktifkan agar tidak digunakan dalam transaksi baru, tetapi riwayat penjualan tetap tersedia.

### 3.5 Manajemen Layanan

Admin dapat membuat, mengubah, mengaktifkan, dan menonaktifkan layanan.

Setiap layanan sekurang-kurangnya memiliki:

- Nama layanan.
- Deskripsi.
- Harga.
- Status aktif atau tidak aktif.

Contoh layanan meliputi konsultasi, pemeriksaan, vaksinasi, pengobatan, dan grooming jika memang disediakan klinik.

Perubahan harga berlaku untuk transaksi baru. Transaksi terdahulu harus tetap menyimpan harga yang berlaku pada saat transaksi dilakukan.

### 3.6 Sistem Kasir (POS)

Sistem kasir menjadi fitur utama untuk operasional klinik.

Alur transaksi:

1. Kasir membuka halaman transaksi baru.
2. Kasir memilih pasien hewan jika transaksi ingin dihubungkan dengan pasien.
3. Kasir memilih satu atau beberapa obat dan layanan.
4. Kasir memasukkan jumlah setiap item.
5. Sistem menghitung subtotal setiap item dan total sementara.
6. Kasir memasukkan diskon atau biaya tambahan jika diperlukan.
7. Sistem menghitung total akhir.
8. Kasir memilih metode pembayaran.
9. Pembayaran harus lunas sebelum transaksi diselesaikan.
10. Sistem menyimpan transaksi, memperbarui stok, dan menyediakan nota PDF.

Satu transaksi dapat berisi beberapa obat dan beberapa layanan sekaligus.

Transaksi juga boleh dibuat tanpa data pasien, termasuk penjualan obat biasa.

Metode pembayaran yang didukung:

- Tunai.
- Transfer bank.
- QRIS.
- Metode lainnya yang dicatat oleh kasir.

Sistem tidak menyediakan pembayaran sebagian atau pencatatan utang.

### 3.7 Perhitungan Transaksi

Sistem menggunakan perhitungan berikut:

- Subtotal item = jumlah × harga satuan.
- Subtotal transaksi = jumlah seluruh subtotal item.
- Total akhir = subtotal transaksi − diskon + biaya tambahan.

Diskon dan biaya tambahan bersifat opsional. Jika tidak dimasukkan, nilainya dianggap nol.

Harga item harus disimpan sebagai nilai transaksi agar perubahan harga obat atau layanan di kemudian hari tidak mengubah nota dan laporan historis.

### 3.8 Nota Pembayaran PDF

Setiap transaksi yang selesai memiliki nomor nota unik.

Nota memuat:

- Logo klinik.
- Nama klinik.
- Alamat klinik.
- Nomor nota.
- Tanggal dan waktu transaksi.
- Nama hewan dan pemilik jika pasien dipilih.
- Rincian obat dan layanan.
- Jumlah setiap item.
- Harga satuan.
- Subtotal.
- Diskon dan biaya tambahan.
- Total pembayaran.
- Metode pembayaran.

Nota dapat diunduh dan dicetak melalui PDF. Nota lama dapat diunduh ulang dari riwayat transaksi.

Harga modal dan laba tidak ditampilkan pada nota pelanggan.

### 3.9 Riwayat Transaksi dan Audit Trail

Sistem menyediakan halaman riwayat transaksi dengan kemampuan:

- Mencari berdasarkan nomor nota, pasien, atau pemilik.
- Memfilter transaksi berdasarkan tanggal.
- Melihat rincian setiap transaksi.
- Mengunduh ulang nota PDF.
- Membedakan transaksi selesai dan dibatalkan.
- Melihat riwayat perubahan transaksi.

Kasir dan admin dapat mengubah atau membatalkan transaksi sesuai izin yang diberikan.

Setiap perubahan atau pembatalan harus mencatat:

- Pengguna yang melakukan tindakan.
- Waktu tindakan.
- Jenis tindakan.
- Data sebelum dan sesudah perubahan jika relevan.
- Alasan perubahan atau pembatalan jika diwajibkan oleh kebijakan sistem.

Riwayat audit tidak boleh dapat diubah atau dihapus melalui fungsi operasional biasa.

Pembatalan transaksi harus menangani penyesuaian stok secara konsisten. Catatan transaksi yang dibatalkan tetap disimpan.

### 3.10 Dashboard dan Laporan

Dashboard admin menyediakan ringkasan kegiatan klinik dan akses ke laporan berikut.

**A. Laporan transaksi harian**

- Daftar transaksi pada tanggal yang dipilih.
- Jumlah transaksi selesai dan dibatalkan.
- Total pendapatan transaksi yang selesai.

**B. Laporan pendapatan bulanan**

- Ringkasan pendapatan per bulan.
- Jumlah transaksi.
- Filter periode yang relevan.

**C. Laporan penjualan obat**

- Nama obat.
- Jumlah terjual.
- Nilai penjualan.
- Pengelompokan berdasarkan periode.

**D. Laporan stok obat**

- Stok tersedia.
- Stok minimum.
- Obat yang mencapai atau berada di bawah batas minimum.
- Riwayat stok masuk dan keluar.

**E. Laporan layanan**

- Jumlah setiap layanan yang diberikan.
- Nilai pendapatan setiap layanan.
- Filter periode.

**F. Laporan laba penjualan obat**

- Nilai penjualan obat.
- Harga modal yang tersimpan pada transaksi atau dasar modal yang ditetapkan sistem.
- Estimasi laba kotor penjualan obat.

Laporan laba harus menggunakan data transaksi yang konsisten dan tidak menghitung transaksi yang dibatalkan sebagai penjualan aktif.

Laporan laba bersih seluruh klinik tidak termasuk kebutuhan awal karena biaya operasional seperti gaji, listrik, sewa, dan pengeluaran lainnya belum dimasukkan ke dalam cakupan.

### 3.11 Pengelolaan Konten Website

Admin dapat mengelola seluruh konten publik melalui dashboard tanpa mengedit kode program.

Konten meliputi:

- Profil klinik.
- Logo dan informasi kontak.
- Alamat dan jam operasional.
- Profil dokter hewan.
- Daftar layanan dan harga.
- Informasi obat.
- Artikel kesehatan hewan.
- Konten beranda.

Konten yang tidak aktif atau diarsipkan tidak ditampilkan kepada pengunjung, tetapi tetap dapat dikelola admin sesuai kebijakan penyimpanan data.

### 3.12 Pengelolaan Pengguna

Admin dapat membuat akun kasir, memperbarui informasi akun, mengatur status aktif atau tidak aktif, dan mengelola hak akses.

Akun yang dinonaktifkan tidak dapat login, sedangkan riwayat transaksi yang pernah dibuat oleh akun tersebut tetap tersimpan.

### 3.13 Backup Data

Sistem harus mendukung pencadangan otomatis secara berkala.

Backup harus mencakup database serta file penting yang dibutuhkan untuk memulihkan aplikasi, sesuai konfigurasi penyimpanan.

Prosedur pemulihan harus diuji agar backup tidak hanya tersedia, tetapi benar-benar dapat digunakan untuk memulihkan data.

---

## 4. DI LUAR CAKUPAN

Fitur berikut tidak termasuk dalam versi awal produk:

1. Aplikasi Android atau iOS khusus.
2. Multi-cabang atau pengelolaan banyak klinik.
3. Sistem rekam medis klinis lengkap dengan diagnosis terstruktur, resep elektronik, dan protokol pengobatan.
4. Reservasi dengan kalender, konfirmasi otomatis, dan manajemen jadwal di dalam aplikasi.
5. Pembayaran online melalui payment gateway.
6. Pembayaran sebagian, utang, cicilan, dan pengelolaan piutang.
7. Integrasi langsung dengan bank atau sistem QRIS untuk verifikasi pembayaran otomatis.
8. Integrasi dengan printer kasir khusus atau perangkat POS melalui protokol khusus.
9. Akuntansi lengkap, penggajian, dan laporan laba bersih klinik.
10. Pengadaan obat otomatis dari pemasok.
11. Pengelolaan kedaluwarsa obat dan nomor batch sebagai fitur wajib pada versi awal.
12. Sistem notifikasi otomatis melalui SMS atau WhatsApp API.
13. Portal akun khusus untuk pemilik hewan.
14. Telekonsultasi dan konsultasi dokter hewan melalui video.
15. Pengelolaan klaim asuransi hewan.

Fitur di luar cakupan dapat dipertimbangkan pada versi berikutnya setelah kebutuhan operasional utama berjalan stabil.

---

## 5. BATASAN

### 5.1 Batasan Teknologi

- Backend menggunakan Laravel.
- Lingkungan pengembangan lokal menggunakan Laravel Herd.
- Database menggunakan SQLite pada tahap awal.
- Antarmuka menggunakan teknologi web yang kompatibel dengan Laravel.
- Aplikasi harus dapat dijalankan melalui browser modern.
- Desain harus responsif untuk komputer, laptop, dan ponsel.

### 5.2 Batasan Deployment

Laravel Herd merupakan lingkungan pengembangan lokal, bukan layanan hosting produksi.

Agar aplikasi dapat diakses secara online, aplikasi harus di-deploy ke server atau layanan hosting yang mendukung Laravel.

Penggunaan SQLite di lingkungan produksi harus mempertimbangkan jumlah pengguna bersamaan, mekanisme penguncian database, penyimpanan persisten, dan proses backup.

Apabila kebutuhan akses bersamaan atau beban operasional berkembang, migrasi ke database server seperti MySQL atau PostgreSQL dapat dipertimbangkan.

### 5.3 Batasan Operasional

- Versi awal hanya melayani satu klinik.
- Pengunjung tidak membutuhkan akun.
- Admin dan kasir harus login untuk mengakses dashboard.
- Pembayaran harus lunas sebelum transaksi diselesaikan.
- Reservasi dilakukan melalui WhatsApp, bukan diproses sebagai booking internal.
- Seluruh harga dan stok harus dikelola melalui sistem.
- Laporan bergantung pada ketepatan data transaksi, harga modal, dan stok.
- Data transaksi historis harus tetap konsisten setelah perubahan harga.

### 5.4 Batasan Keamanan

- Kata sandi harus disimpan menggunakan mekanisme hashing yang aman.
- Akses fitur harus diperiksa di sisi server.
- Validasi input harus dilakukan sebelum data disimpan.
- Data transaksi dan pasien tidak boleh tersedia secara publik.
- Nomor nota harus unik.
- Perubahan stok dan transaksi harus konsisten meskipun terjadi kegagalan proses.
- File backup harus dilindungi dari akses publik yang tidak berwenang.
- Koneksi produksi harus menggunakan HTTPS.
- Penghapusan data yang berkaitan dengan transaksi harus dibatasi untuk menjaga integritas laporan.

### 5.5 Batasan Data

- Pasien dan transaksi diarsipkan, bukan dihapus permanen melalui fungsi operasional biasa.
- Obat dan layanan yang belum pernah digunakan dalam transaksi boleh dihapus.
- Obat dan layanan yang memiliki riwayat transaksi harus dinonaktifkan jika tidak lagi digunakan.
- Riwayat transaksi dan audit trail harus dipertahankan.
- Harga modal dan harga jual harus dibedakan.
- Laporan laba pada versi awal berfokus pada laba kotor penjualan obat.

---

## 6. KRITERIA PENERIMAAN

Produk dianggap memenuhi kebutuhan versi awal jika kriteria berikut berhasil diuji.

### 6.1 Website Publik

- [ ] Seluruh halaman publik dapat dibuka tanpa login.
- [ ] Profil klinik, layanan, harga, informasi obat, dokter, artikel, dan kontak ditampilkan dengan benar.
- [ ] Tombol reservasi membuka WhatsApp klinik dengan nomor tujuan yang benar.
- [ ] Pesan reservasi awal dapat terisi otomatis dan dapat diedit pengunjung.
- [ ] Halaman berfungsi dengan baik pada komputer, laptop, dan ponsel.
- [ ] Perubahan konten yang dilakukan admin ditampilkan pada website tanpa mengedit kode program.

### 6.2 Login dan Hak Akses

- [ ] Admin dapat login dan mengakses seluruh fitur yang diizinkan.
- [ ] Kasir dapat login dan mengakses fitur operasional sesuai hak aksesnya.
- [ ] Kasir tidak dapat mengakses fungsi admin yang dilarang, termasuk melalui URL atau permintaan langsung ke server.
- [ ] Pengunjung tanpa login tidak dapat mengakses dashboard atau data internal.
- [ ] Akun yang dinonaktifkan tidak dapat login.

### 6.3 Data Pasien

- [ ] Sistem dapat menyimpan seluruh kolom pasien yang ditetapkan dalam PRD.
- [ ] Keterangan tambahan dapat diisi dengan teks bebas.
- [ ] Pasien dapat dicari dan diperbarui.
- [ ] Riwayat pemeriksaan dapat ditampilkan berdasarkan pasien.
- [ ] Pasien dapat diarsipkan tanpa menghilangkan riwayat transaksi yang terkait.

### 6.4 Obat dan Stok

- [ ] Admin dapat menambahkan obat beserta harga modal, harga jual, dan stok awal.
- [ ] Sistem mencatat stok masuk, stok keluar, dan penyesuaian stok.
- [ ] Setiap perubahan stok menghasilkan catatan riwayat yang sesuai.
- [ ] Sistem menampilkan indikator stok minimum.
- [ ] Transaksi selesai mengurangi stok sesuai jumlah yang terjual.
- [ ] Sistem menolak transaksi jika jumlah yang diminta melebihi stok tersedia.
- [ ] Pembatalan transaksi mengembalikan stok sesuai jumlah yang sebelumnya dikurangi.
- [ ] Perubahan harga obat tidak mengubah rincian harga pada transaksi lama.

### 6.5 Layanan

- [ ] Admin dapat menambahkan, mengubah, mengaktifkan, dan menonaktifkan layanan.
- [ ] Harga layanan yang aktif dapat digunakan dalam transaksi baru.
- [ ] Transaksi lama tetap menyimpan harga saat transaksi dibuat.
- [ ] Layanan yang sudah digunakan dalam transaksi tidak dapat dihapus secara permanen melalui fungsi biasa.

### 6.6 Transaksi Kasir

- [ ] Kasir dapat membuat transaksi dengan beberapa obat dan layanan sekaligus.
- [ ] Transaksi dapat dibuat tanpa memilih pasien.
- [ ] Sistem menghitung jumlah, harga satuan, subtotal, diskon, biaya tambahan, dan total akhir secara benar.
- [ ] Sistem menerima metode pembayaran tunai, transfer, QRIS, dan metode lainnya.
- [ ] Sistem tidak menyelesaikan transaksi sebelum pembayaran lunas dikonfirmasi oleh kasir.
- [ ] Transaksi yang berhasil disimpan memiliki nomor nota unik.
- [ ] Data transaksi, perubahan stok, dan status pembayaran tersimpan secara konsisten.
- [ ] Kegagalan proses tidak menyebabkan stok berkurang tanpa transaksi yang sesuai atau transaksi tersimpan tanpa penyesuaian stok yang semestinya.

### 6.7 Nota PDF

- [ ] Nota dapat diunduh dan dibuka sebagai file PDF yang valid.
- [ ] Nota memuat logo, identitas klinik, nomor nota, tanggal dan waktu, rincian item, jumlah, harga, subtotal, diskon atau biaya tambahan, total, dan metode pembayaran.
- [ ] Data pasien hanya ditampilkan jika pasien dipilih pada transaksi.
- [ ] Harga modal dan laba tidak ditampilkan pada nota pelanggan.
- [ ] Nota transaksi lama dapat diunduh ulang tanpa mengubah data transaksi.

### 6.8 Riwayat Transaksi dan Audit Trail

- [ ] Transaksi dapat dicari berdasarkan nomor nota, nama hewan, atau nama pemilik.
- [ ] Transaksi dapat difilter berdasarkan tanggal.
- [ ] Detail transaksi dapat dibuka kembali.
- [ ] Status transaksi selesai dan dibatalkan ditampilkan dengan jelas.
- [ ] Kasir dan admin dapat melakukan perubahan atau pembatalan sesuai hak akses.
- [ ] Setiap perubahan dan pembatalan mencatat pengguna, waktu, jenis tindakan, serta rincian perubahan yang relevan.
- [ ] Transaksi yang dibatalkan tetap tersedia sebagai catatan historis.
- [ ] Pembatalan tidak menghasilkan pengurangan atau pengembalian stok secara ganda.

### 6.9 Laporan

- [ ] Laporan transaksi harian menampilkan transaksi sesuai tanggal yang dipilih.
- [ ] Laporan pendapatan bulanan menampilkan ringkasan sesuai bulan atau periode.
- [ ] Laporan penjualan obat menampilkan jumlah dan nilai penjualan.
- [ ] Laporan stok menampilkan stok tersedia, batas minimum, dan obat yang perlu ditambah.
- [ ] Laporan layanan menampilkan jumlah layanan dan nilai pendapatan.
- [ ] Laporan laba obat menggunakan harga modal yang sesuai dengan dasar perhitungan yang ditetapkan.
- [ ] Transaksi yang dibatalkan tidak dihitung sebagai penjualan aktif.
- [ ] Nilai laporan sesuai dengan transaksi yang tersimpan pada database.

### 6.10 Pengelolaan Data dan Backup

- [ ] Obat atau layanan yang belum pernah digunakan dalam transaksi dapat dihapus.
- [ ] Obat atau layanan yang sudah memiliki riwayat transaksi dapat dinonaktifkan tanpa merusak laporan historis.
- [ ] Data transaksi dan pasien dapat diarsipkan sesuai kebijakan sistem.
- [ ] Backup berjalan sesuai jadwal yang ditetapkan.
- [ ] Backup dapat dipulihkan pada lingkungan pengujian.
- [ ] Pemulihan backup menghasilkan data pasien, transaksi, stok, dan riwayat yang konsisten.

---

**Definisi selesai:** Produk versi awal dinyatakan siap digunakan setelah seluruh kriteria penerimaan yang relevan lulus pengujian, masalah keamanan kritis ditangani, proses backup dan pemulihan berhasil diuji, serta aplikasi berhasil di-deploy ke lingkungan online yang sesuai.
