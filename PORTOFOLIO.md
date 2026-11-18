# PORTOFOLIO INDIVIDU
## Project Akhir Sistem Operasi
### Pilihan 5B — Sistem Antrean Pekerjaan dan Monitoring Proses Linux

---

## 1. Identitas

| Keterangan | Informasi |
|---|---|
| Nama Lengkap | Muhammad Fathir Natadiwangsa |
| NIM | 2510512183 |
| Kelas | Kelas E |
| Kelompok | Kelompok 5 |
| Mata Kuliah | Sistem Operasi |
| Judul Proyek | Pilihan 5B — Sistem Antrean Pekerjaan dan Monitoring Proses Linux |
| Nama Proyek | proyek-so |

---

## 2. Asal Proyek

Proyek **Sistem Antrean Pekerjaan dan Monitoring Proses Linux** merupakan tugas Project Akhir mata kuliah Sistem Operasi dengan pilihan topik 5B. Proyek ini dikerjakan secara berkelompok dengan tujuan menerapkan konsep sistem operasi Linux, khususnya pengelolaan proses, eksekusi pekerjaan, pemantauan proses, serta pengendalian pekerjaan berdasarkan batas waktu.

Proyek ini merupakan hasil kerja sama enam anggota kelompok, sehingga keseluruhan sistem, dokumentasi, dan hasil implementasinya merupakan tanggung jawab bersama. Portofolio ini secara khusus menjelaskan bagian pekerjaan yang saya kerjakan dan kontribusi yang saya berikan selama proses pengerjaan proyek.

**Repository Utama Kelompok:**

https://github.com/iiqbalitoo/proyekSO_5B_Kel5

**Daftar Anggota Kelompok:**

1. Muhammad Iqbal Rizqullah
2. Harsya Maulana Syahbani
3. Ananda Hafiz Aulia
4. Muhammad Fathir Natadiwangsa
5. Rifqi Naufal Anwar
6. Waldan Nur Rabbani

---

## 3. Kontribusi Pribadi

Dalam pengerjaan proyek ini, saya bertanggung jawab pada bagian pengujian dan dokumentasi penghentian proses berdasarkan batas waktu (*timeout*) menggunakan skrip `timeout.sh`.

Adapun kontribusi yang saya berikan meliputi:

1. **Pengujian timeout.sh**  
   Melakukan pengujian terhadap mekanisme penghentian proses berdasarkan batas waktu untuk memastikan pekerjaan yang selesai sebelum batas waktu dapat berjalan normal dan pekerjaan yang melewati batas waktu dapat dihentikan.

2. **Pengujian Kondisi Positif dan Negatif**  
   Menjalankan dua skenario pengujian, yaitu pekerjaan yang selesai dalam waktu kurang dari batas yang ditentukan dan pekerjaan yang melebihi batas waktu.

3. **Dokumentasi Hasil Pengujian**  
   Mencatat hasil pengujian ke dalam berkas `evidence/fathir-positif.txt` dan `evidence/fathir-negatif.txt`, termasuk exit status dan pemeriksaan proses yang masih berjalan.

4. **Penyusunan Laporan**  
   Menyusun Subbab 3.4 dengan judul Penghentian Proses (`timeout.sh`) pada laporan akhir kelompok.

5. **Pengisian Matriks Kontribusi**  
   Membantu melengkapi matriks kontribusi sebagai dokumentasi pembagian tugas dan tanggung jawab masing-masing anggota kelompok.

---

## 4. Bukti Kontribusi

Kontribusi saya dapat dilihat melalui beberapa bukti yang terdapat pada repository utama kelompok.

### 4.1 Bukti Commit GitHub

Saya melakukan pengiriman perubahan ke repository utama kelompok melalui commit dengan pesan:

**"Bukti Fathir"**

Link commit:

https://github.com/iiqbalitoo/proyekSO_5B_Kel5/commit/19fe5b6cd5b0ed01ec7c7cb13975f038f4e12073

### 4.2 Berkas Evidence

Bukti pengujian yang saya dokumentasikan terdiri dari:

| Nama Berkas | Keterangan |
|---|---|
| `evidence/fathir-positif.txt` | Dokumentasi pengujian ketika pekerjaan selesai sebelum batas waktu. |
| `evidence/fathir-negatif.txt` | Dokumentasi pengujian ketika pekerjaan melewati batas waktu dan dihentikan. |

### 4.3 Bukti Dokumentasi Laporan

Selain bukti berupa commit dan berkas pengujian, kontribusi saya juga terdapat pada:

- Laporan akhir kelompok, Subbab 3.4 Penghentian Proses (`timeout.sh`).
- Matriks Kontribusi yang mencatat pembagian pekerjaan anggota kelompok.
- Tangkapan layar hasil pengujian kondisi positif dan negatif.

Bukti-bukti tersebut digunakan untuk menunjukkan bagian pekerjaan yang saya lakukan selama pengerjaan proyek.

---

## 5. Skenario Individu

### 5.1 Tujuan Pengujian

Pengujian individu dilakukan untuk memastikan bahwa mekanisme penghentian proses berdasarkan batas waktu dapat bekerja sesuai dengan fungsinya.

Tujuan utamanya adalah memastikan pekerjaan yang selesai sebelum batas waktu dapat berjalan secara normal, sedangkan pekerjaan yang melebihi batas waktu dapat dihentikan secara terkendali tanpa menyisakan proses yang masih berjalan.

### 5.2 Pengujian Kondisi Positif

**Skenario:** Pekerjaan selesai sebelum batas waktu.

Perintah yang digunakan:

```bash
bash scripts/timeout.sh 5 tests/tidur.sh 2
```

Keterangan:

- `5` merupakan batas waktu maksimal eksekusi dalam detik.
- `tests/tidur.sh` merupakan skrip pekerjaan yang dijalankan.
- `2` merupakan durasi pekerjaan selama 2 detik.

Pada pengujian ini, pekerjaan dijalankan selama 2 detik dengan batas waktu 5 detik. Karena durasi pekerjaan lebih singkat daripada batas waktu, proses diharapkan dapat selesai secara normal tanpa dihentikan oleh mekanisme timeout.

**Hasil yang diperiksa:**

1. Pekerjaan dapat dijalankan dengan normal.
2. Proses selesai sebelum batas waktu 5 detik.
3. Exit status menunjukkan bahwa pekerjaan berhasil diselesaikan.

### 5.3 Pengujian Kondisi Negatif

**Skenario:** Pekerjaan melewati batas waktu.

Perintah yang digunakan:

```bash
bash scripts/timeout.sh 5 tests/tidur.sh 10
```

Keterangan:

- `5` merupakan batas waktu maksimal eksekusi dalam detik.
- `tests/tidur.sh` merupakan skrip pekerjaan yang dijalankan.
- `10` merupakan durasi pekerjaan selama 10 detik.

Pada pengujian ini, pekerjaan dijalankan selama 10 detik dengan batas waktu maksimal 5 detik. Karena durasi pekerjaan melebihi batas waktu, mekanisme timeout diharapkan menghentikan proses tersebut.

**Hasil yang diperiksa:**

1. Proses dihentikan ketika melewati batas waktu.
2. Exit status menunjukkan nilai `124` sebagai penanda timeout.
3. Dilakukan pemeriksaan proses menggunakan perintah:

```bash
ps aux | grep tidur
```

4. Pemeriksaan dilakukan untuk memastikan tidak terdapat proses pekerjaan `tidur` yang masih berjalan setelah penghentian.

### 5.4 Verifikasi Pengujian

Verifikasi dilakukan berdasarkan hasil eksekusi perintah, nilai exit status, serta pemeriksaan proses yang masih berjalan.

Hasil pengujian dan tangkapan layar didokumentasikan dalam berkas evidence sebagai bukti bahwa kedua skenario telah diuji.

| Skenario | Durasi Pekerjaan | Batas Waktu | Hasil yang Diharapkan |
|---|---:|---:|---|
| Positif | 2 detik | 5 detik | Pekerjaan selesai normal. |
| Negatif | 10 detik | 5 detik | Pekerjaan dihentikan karena timeout dengan exit status 124. |

---

## 6. Analisis Konsep Sistem Operasi

Berdasarkan pengujian yang dilakukan, terdapat beberapa konsep Sistem Operasi yang dapat dipahami dan diterapkan dalam mekanisme penghentian proses menggunakan `timeout.sh`.

### 6.1 Siklus Hidup Proses (Process Life Cycle)

Setiap pekerjaan yang dijalankan di Linux akan melalui siklus hidup proses, mulai dari proses dibuat, dieksekusi, hingga selesai atau dihentikan.

Pada pengujian kondisi positif, proses dapat menyelesaikan pekerjaannya secara normal sebelum batas waktu. Sementara itu, pada kondisi negatif, proses harus dihentikan karena waktu eksekusinya telah melewati batas yang ditentukan.

Hal ini menunjukkan bahwa sistem operasi memiliki mekanisme untuk mengelola proses selama proses tersebut berjalan.

### 6.2 Pengiriman Sinyal (Signal)

Linux menyediakan mekanisme pengiriman sinyal untuk mengendalikan proses yang sedang berjalan.

Dalam mekanisme timeout, sinyal dapat digunakan untuk meminta proses berhenti ketika melewati batas waktu. Jika proses tidak berhenti setelah menerima sinyal penghentian awal, mekanisme penghentian paksa dapat digunakan sesuai implementasi skrip.

Dengan demikian, penggunaan signal membantu mengendalikan proses agar tidak berjalan melebihi waktu yang telah ditentukan.

### 6.3 Exit Status 124

Exit status merupakan nilai yang dikembalikan oleh suatu proses setelah selesai dieksekusi.

Pada pengujian kondisi negatif, nilai exit status `124` digunakan sebagai penanda bahwa proses dihentikan karena melewati batas waktu oleh mekanisme timeout.

Nilai tersebut membantu pengguna mengetahui bahwa pekerjaan tidak selesai secara normal, melainkan dihentikan karena batas waktu eksekusi telah tercapai.

### 6.4 Kebersihan Tabel Proses

Setelah suatu proses dihentikan, penting untuk memastikan bahwa tidak ada proses pekerjaan yang masih berjalan tanpa diperlukan.

Pemeriksaan menggunakan perintah `ps aux | grep tidur` dilakukan untuk melihat apakah proses yang berkaitan dengan pekerjaan tersebut masih aktif.

Hal ini berkaitan dengan pengelolaan proses dalam sistem operasi, termasuk memastikan proses anak ditangani dengan benar dan tidak meninggalkan proses yang tidak diperlukan.

Perlu dipahami bahwa proses zombie berbeda dengan proses yang masih berjalan. Proses zombie sudah selesai dieksekusi, tetapi entri prosesnya masih menunggu untuk diambil status akhirnya oleh proses induk (*parent process*).

Oleh karena itu, pemeriksaan proses menjadi bagian penting dalam memastikan mekanisme penghentian berjalan dengan baik.

---

## 7. Kendala dan Penyelesaian

Selama pengerjaan proyek, saya mengalami kendala ketika melakukan sinkronisasi repository lokal dengan repository utama kelompok di GitHub.

### 7.1 Kendala yang Dihadapi

Kendala utama yang terjadi adalah branch lokal tertinggal dari repository remote sehingga muncul kondisi `non-fast-forward` ketika melakukan push.

Hal tersebut terjadi karena terdapat commit baru pada repository GitHub yang belum terdapat pada repository lokal.

Selain itu, proses pembaruan sempat terhambat karena terdapat perubahan file lokal yang belum disimpan atau masih berstatus *unstaged changes*. Kondisi tersebut menyebabkan proses `git pull --rebase` tidak dapat langsung dilakukan.

### 7.2 Langkah Penyelesaian

Untuk mengatasi kendala tersebut, saya melakukan beberapa langkah berikut:

**1. Mengamankan perubahan lokal sementara**

```bash
git stash
```

Perintah ini digunakan untuk menyimpan sementara perubahan lokal agar tidak mengganggu proses pembaruan repository.

**2. Mengambil pembaruan dari repository remote**

```bash
git pull --rebase origin main
```

Perintah ini digunakan untuk mengambil commit terbaru dari branch `main` sekaligus menyesuaikan perubahan lokal dengan riwayat commit remote.

**3. Mengembalikan perubahan lokal**

```bash
git stash pop
```

Perintah ini digunakan untuk mengembalikan perubahan yang sebelumnya disimpan menggunakan `git stash`.

**4. Mengirim perubahan ke repository utama**

```bash
git push origin main
```

Perintah ini digunakan untuk mengirimkan perubahan lokal ke repository utama kelompok.

Apabila GitHub meminta autentikasi melalui HTTPS, Personal Access Token (PAT) digunakan sebagai pengganti password akun GitHub.

### 7.3 Hasil Penyelesaian

Melalui langkah-langkah tersebut, saya dapat memahami cara menangani konflik sinkronisasi antara repository lokal dan remote.

Kendala ini memberikan pengalaman tambahan dalam penggunaan Git, khususnya dalam mengamankan perubahan lokal, memperbarui riwayat commit, serta mengirimkan perubahan ke repository bersama.

---

## 8. Refleksi

### 8.1 Hal yang Sudah Dikuasai

Selama pengerjaan proyek ini, saya memperoleh pemahaman dan pengalaman dalam beberapa hal, yaitu:

1. Memahami penggunaan skrip Bash untuk menjalankan pekerjaan di lingkungan Linux.
2. Memahami dasar mekanisme timeout untuk membatasi durasi eksekusi suatu proses.
3. Melakukan pengujian kondisi positif dan negatif pada proses yang dijalankan.
4. Memahami penggunaan exit status sebagai indikator hasil eksekusi program.
5. Menggunakan perintah Linux seperti `ps aux` untuk memeriksa proses yang sedang berjalan.
6. Memahami dasar penggunaan Git dan GitHub untuk mengelola serta mengirimkan perubahan proyek.
7. Menyusun dokumentasi hasil pengujian dan menghubungkannya dengan konsep Sistem Operasi.

### 8.2 Hal yang Masih Perlu Dipelajari

Meskipun telah memahami dasar pengujian penghentian proses, masih terdapat beberapa hal yang perlu saya pelajari lebih lanjut, yaitu:

1. Memahami lebih dalam mekanisme pengiriman signal di Linux, termasuk perbedaan `SIGTERM` dan `SIGKILL`.
2. Mempelajari pengelolaan proses induk dan anak (*parent-child process*) agar lebih memahami bagaimana proses yang dihentikan dapat ditangani dengan benar.
3. Memahami lebih detail penyebab dan penanganan proses zombie.
4. Meningkatkan kemampuan dalam menulis skrip Bash yang lebih aman dan mampu menangani berbagai kondisi kesalahan.
5. Memperdalam penggunaan Git, khususnya dalam menangani konflik ketika melakukan merge maupun rebase.

### 8.3 Kesimpulan Refleksi

Melalui proyek ini, saya mendapatkan pengalaman langsung dalam menerapkan konsep Sistem Operasi Linux, terutama pada pengelolaan dan penghentian proses berdasarkan batas waktu.

Saya menyadari bahwa pemahaman teori saja belum cukup tanpa melakukan pengujian secara langsung. Melalui dua skenario pengujian, saya dapat memahami bagaimana proses berjalan secara normal maupun dihentikan ketika melewati batas waktu.

Selain aspek teknis, proyek ini juga memberikan pengalaman dalam bekerja secara berkelompok, menyusun dokumentasi, membagi tanggung jawab, serta menggunakan GitHub sebagai media kolaborasi.

Ke depannya, saya perlu meningkatkan pemahaman mengenai manajemen proses dan mekanisme signal Linux agar dapat mengimplementasikan sistem pengelolaan proses dengan lebih baik.

---

**Catatan:** Portofolio ini disusun berdasarkan kontribusi pribadi Muhammad Fathir Natadiwangsa dalam proyek kelompok Pilihan 5B. Seluruh sistem dan hasil akhir proyek merupakan hasil kerja sama anggota Kelompok 5, sedangkan bagian yang dijelaskan secara khusus dalam portofolio ini merupakan pekerjaan yang saya tangani secara langsung.
