# Nama   : Muhammad Aqia Yudha Yulian Putra
<br>

# NIM    : 2509116105
<br>

# Kelas  : C Sistem Informasi
<br>

# Matkul : PBO
<br> 

# SISTEM PENYEWAAN ALAT MUSIK

## 1. Deskripsi Singkat Program
Sistem Penyewaan Alat Musik merupakan program CLI (*Command Line Interface*) berbasis Java yang dirancang untuk mengelola data instrumen musik pada sebuah usaha penyewaan/rental. Data instrumen dikelompokkan menjadi dua jenis spesifik, yaitu **Alat Musik Petik** dan **Alat Musik Pukul**. Program ini menggunakan struktur data koleksi **ArrayList** untuk menyimpan dan memanipulasi data selama program berjalan (berada di dalam memori).

Program ini telah mengimplementasikan konsep-konsep fundamental *Object-Oriented Programming* (OOP) dan logika dasar, meliputi:
- **Inheritance (Pewarisan):** Memiliki satu *superclass* (`InstrumenMusik`) dan dua *subclass* (`AlatMusikPetik` dan `AlatMusikPukul`).
- **Polymorphism:** Menggunakan *Method Overriding* untuk membedakan format cetak detail tiap jenis instrumen.
- **Condition (Percabangan):** Menggunakan `If-Else` dan `Switch-Case` untuk navigasi menu dan validasi ID.
- **Looping (Perulangan):** Menggunakan `While` untuk mempertahankan menu tetap berjalan dan `For/For-each` untuk membaca data di dalam ArrayList.

## 2. Penjelasan Alur Program Terperinci
Ketika program pertama kali dijalankan, sistem secara otomatis akan memuat *dummy data* awal ke dalam ArrayList agar daftar tidak kosong. Selanjutnya, sistem akan masuk ke dalam perulangan menu utama yang menawarkan 5 opsi interaktif. Berikut adalah alur eksekusi untuk masing-masing menu:

### A. Menu 1: Tampilkan Daftar Instrumen (Read)
Sistem melakukan perulangan pada ArrayList untuk mengambil seluruh objek alat musik yang tersimpan. 
- Berkat penerapan *Polymorphism*, sistem secara dinamis mencetak format yang berbeda tergantung jenis objeknya.
- Jika instrumen adalah **Alat Musik Petik**, sistem akan menampilkan detail tambahan berupa `Jumlah Senar`.
- Jika instrumen adalah **Alat Musik Pukul**, sistem akan menampilkan detail tambahan berupa `Material Bahan`.

### B. Menu 2: Tambah Instrumen Baru (Create)
Program meminta pengguna untuk menginputkan data dasar yang berlaku untuk semua instrumen, yaitu `ID Alat`, `Merk`, dan `Harga Sewa/Hari`.
- Setelah itu, sistem menggunakan percabangan (`if-else`) untuk meminta pengguna memilih kategori alat musik:
  1. **Alat Musik Petik:** Meminta input khusus `Jumlah Senar`.
  2. **Alat Musik Pukul:** Meminta input khusus `Material Bahan`.
- Setelah semua data terkumpul, program menginstansiasi (membuat objek baru) dari subclass yang dipilih dan menyimpannya ke posisi terbawah di dalam ArrayList menggunakan method `.add()`.

### C. Menu 3: Ubah Data Instrumen (Update)
Sistem meminta pengguna memasukkan `ID Alat` yang ingin diperbarui.
- Program kemudian melakukan perulangan untuk mencari kecocokan ID tersebut di dalam ArrayList.
- Jika ID ditemukan, pengguna dipersilakan memasukkan `Merk Baru` dan `Harga Sewa Baru`. Atribut pada objek tersebut kemudian ditimpa dengan nilai yang baru secara langsung.
- Jika ID tidak ditemukan, sistem akan menampilkan pesan peringatan bahwa data tidak ada.

### D. Menu 4: Hapus Instrumen (Delete)
Sama seperti fitur Ubah, sistem meminta input `ID Alat` dan mencarinya di dalam ArrayList.
- Jika objek dengan ID tersebut ditemukan, sistem akan memanggil method `.remove()` berdasarkan indeks keberadaan data tersebut untuk menghapusnya secara permanen dari daftar memori.
- Daftar instrumen akan otomatis bergeser menyesuaikan data yang dihapus, dan sistem menampilkan pesan sukses.

### E. Menu 5: Keluar
Jika pengguna memilih angka 5, sistem akan memutus perulangan `while` utama. Layar akan berhenti meminta input dan eksekusi program dinyatakan selesai (Terminated).

## 3. Dokumentasi Fitur (CRUD)

Berikut adalah lampiran hasil eksekusi program untuk setiap fitur yang tersedia:

## Program ini memiliki lima menu utama yang merupakan implementasi langsung dari fitur CRUD (Create, Read, Update, Delete), yaitu:

### 1. Tampilkan Daftar Instrumen
Menampilkan seluruh data alat musik yang tersedia beserta *dummy data* bawaan.

<img width="663" height="217" alt="image" src="https://github.com/user-attachments/assets/bda0b8f1-93ff-4ab7-9528-ab8a94914359" />

### 2. Tambah Instrumen Baru
Menambahkan data instrumen musik baru ke dalam sistem penyewaan berdasarkan kategori spesifiknya.

<img width="353" height="351" alt="image" src="https://github.com/user-attachments/assets/f58e12e9-273c-4443-ab57-1cb062065815" />

### 3. Ubah Data Instrumen
Memperbarui informasi seperti merk dan harga sewa dari alat musik yang sudah terdaftar berdasarkan pencarian ID.

<img width="723" height="502" alt="image" src="https://github.com/user-attachments/assets/dc2153e5-63ed-4def-8821-4aa424ee3f33" />

### 4. Hapus Instrumen
Menghapus data instrumen dari sistem secara permanen berdasarkan ID Alat.

<img width="658" height="437" alt="image" src="https://github.com/user-attachments/assets/7cb3c1de-5d38-45ab-acb3-f3fbbf73cbfc" />

### 5. Keluar
Mengakhiri perulangan program utama.

<img width="625" height="266" alt="image" src="https://github.com/user-attachments/assets/18fc5eb0-f6ea-4989-bc26-9daf877d3351" />
