# Laporan pratikum pertemuan 12

### NAMA: NABILA NAJWA SYAKIRA
### NIM: 312510344
### KELAS: TI.25.C5


_________________________________________________________
#### Output 

<img width="1357" height="871" alt="Screenshot 2025-12-07 132819" src="https://github.com/user-attachments/assets/ab942af3-efe8-463d-a981-22050fc49324" />

<img width="1188" height="637" alt="Screenshot 2025-12-07 132837" src="https://github.com/user-attachments/assets/c00f6702-2bb7-471a-adeb-61a9a45f17d2" />

<img width="1015" height="704" alt="Screenshot 2025-12-07 132855" src="https://github.com/user-attachments/assets/5c8e260b-1ba5-4027-b209-1c2914fa0d15" />

### Flowchart 
<img width="423" height="635" alt="Screenshot 2025-12-07 024706" src="https://github.com/user-attachments/assets/0586cce4-b65a-4a4a-9e22-1bc709d0341f" />



#### Penjelasan kode 
1. Pembuatan Kelas Mahasiswa dan Struktur Penyimpanan

Program diawali dengan mendefinisikan kelas Mahasiswa, yang berfungsi sebagai wadah utama untuk seluruh operasi pengelolaan data. Pada method _init_, dibuat sebuah list kosong self.data
yang nantinya akan berisi kumpulan informasi mahasiswa dalam format dictionary. Dengan pendekatan ini, segala bentuk penambahan, pengubahan, maupun penghapusan data 
dipusatkan dalam satu struktur sehingga lebih mudah dikelola.

2. Fungsi tambah() untuk Menyisipkan Data Baru

Method tambah() dirancang untuk menerima input berupa identitas mahasiswa (nama dan NIM) serta nilai tugas, UTS, dan UAS. Setelah input diberikan, 
program menghitung nilai akhir berdasarkan proporsi penilaian: 30% untuk tugas, 35% untuk UTS, dan 35% untuk UAS. Seluruh data yang diperoleh kemudian dibungkus
dalam dictionary dan dimasukkan ke list self.data. Program kemudian mengonfirmasi bahwa data tersebut berhasil ditambahkan.

3. Fungsi hapus() untuk Menghilangkan Data

Method hapus() memeriksa apakah nama mahasiswa yang dimasukkan pengguna terdapat dalam daftar. Pencariannya dibuat tidak sensitif terhadap huruf besar maupun kecil.
Jika nama yang dicari ditemukan, maka dictionary yang bersangkutan akan dihapus langsung dari list. Jika tidak ada kecocokan, program memberi tahu bahwa data tersebut tidak tersedia. 
Fitur ini menjaga agar daftar mahasiswa tetap bersih dari data yang tidak diperlukan lagi.

4. Fungsi ubah() untuk Memodifikasi Informasi

Method ubah() digunakan untuk memperbarui informasi mahasiswa tertentu. Program akan mencari nama mahasiswa terlebih dahulu. Jika ditemukan, data lama akan digantikan dengan data baru
sesuai input pengguna, baik itu perubahan NIM atau nilai. Setelah proses pembaruan, nilai akhir juga dihitung ulang. Pada versi kode sebelumnya terdapat kesalahan dalam formula nilai akhir,
namun secara konsep method ini memang dibuat agar pembaruan dapat dilakukan secara fleksibel tanpa harus mengisi ulang semua bagian data.

5. Fungsi tampilkan() untuk Menyuguhkan Data

Method tampilkan() bertanggung jawab menampilkan seluruh data mahasiswa dalam format tabel yang terstruktur. Program mencetak judul kolom dan garis batas terlebih dahulu.
Bila daftar masih kosong, akan tampil pesan bahwa belum ada data. Jika data tersedia, ia akan ditampilkan satu per satu dengan nomor urut menggunakan enumerate(). 
Penyajian tabel dibuat agar informasi mudah dibaca dan tersusun rapi.

6. Menu Utama pada Program

Setelah seluruh method dalam kelas didefinisikan, program melanjutkan ke bagian menu utama menggunakan loop while True.
Pengguna diberikan sejumlah pilihan: menambah data, menampilkan data, menghapus data, memperbarui data, atau keluar dari aplikasi. 
Setiap pilihan terhubung langsung dengan method yang telah dibuat. Validasi input menggunakan try/except ditambahkan untuk mencegah program berhenti akibat kesalahan input pengguna.

Secara ringkas, program ini merupakan contoh implementasi sederhana dari sistem CRUD untuk mengelola data mahasiswa. Fitur-fitur di dalamnya disusun dalam method yang terpisah,
sedangkan menu utama bertugas sebagai pengendali interaksi dengan pengguna. Meskipun sederhana, program ini cukup lengkap sebagai simulasi pengelolaan data berbasis teks.
