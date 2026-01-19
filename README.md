# Flowchart Frontend & Backend Documentation

Dokumentasi ini menjelaskan secara menyeluruh **dasar flowchart**, perbedaannya pada **frontend dan backend**, serta bagaimana flowchart digunakan untuk merancang sistem aplikasi yang terstruktur, aman, dan mudah dikembangkan.

---

##  Apa Itu Flowchart?

Flowchart adalah **diagram alur logika** yang menggambarkan urutan proses, keputusan, dan interaksi dalam sebuah sistem dari awal hingga akhir secara visual.

Flowchart digunakan untuk:
- Memvisualisasikan logika sistem sebelum coding
- Mengurangi kesalahan logika
- Mempermudah kolaborasi tim
- Menjadi dokumentasi teknis jangka panjang

---

##  Tujuan Penggunaan Flowchart

- Menjelaskan alur proses aplikasi secara jelas
- Membantu sinkronisasi antara frontend dan backend
- Menjadi panduan implementasi kode
- Memudahkan debugging dan maintenance

---

##  Simbol Dasar Flowchart

| Simbol | Nama | Fungsi |
|------|------|------|
| Oval | Terminator | Start / End proses |
| Persegi | Process | Proses atau eksekusi |
| Jajar Genjang | Input / Output | Input atau output data |
| Belah Ketupat | Decision | Percabangan logika |
| Panah | Flowline | Arah alur proses |

---

# 🖥️ Flowchart Frontend

## 📘 Pengertian

Flowchart frontend menggambarkan **alur interaksi pengguna (user flow)** dengan antarmuka aplikasi. Fokus utamanya adalah pengalaman pengguna (UI/UX), state aplikasi, dan komunikasi dengan backend.

Flowchart frontend **tidak menangani logika database**, tetapi menentukan bagaimana sistem merespons tindakan pengguna.

---

## 🧩 Komponen Flowchart Frontend

### 1️⃣ User Interaction
- Klik tombol
- Mengisi form
- Navigasi halaman
- Submit data

### 2️⃣ UI State Management
- Loading state
- Error state
- Success state
- Disabled / enabled button

### 3️⃣ Client-Side Validation
Validasi awal sebelum request dikirim ke backend:
- Field tidak boleh kosong
- Format email valid
- Password minimal karakter

### 4️⃣ API Communication
- Mengirim request ke backend
- Menunggu response
- Menampilkan hasil response ke UI

---

## 🔄 Contoh Flowchart Frontend (Login)

1. User membuka halaman login
2. User mengisi email dan password
3. Frontend melakukan validasi input
4. Jika valid → kirim request ke backend
5. Tampilkan loading indicator
6. Terima response:
   - Success → redirect ke dashboard
   - Error → tampilkan pesan error

---

## 🎨 Keuntungan Flowchart Frontend

- UI lebih terstruktur
- UX lebih jelas dan konsisten
- Menghindari alur user yang membingungkan
- Mempermudah implementasi React, Vue, atau Vanilla JS

---

# 🧠 Flowchart Backend

## 📕 Pengertian

Flowchart backend menggambarkan **alur logika server** dalam memproses data dan request dari frontend. Fokus utamanya adalah keamanan, aturan bisnis, dan pengelolaan data.

---

## 🧩 Komponen Flowchart Backend

### 1️⃣ Request Handling
- Menerima request dari frontend
- Validasi HTTP method
- Parsing request body

### 2️⃣ Authentication & Authorization
- Validasi token / session
- Cek hak akses user
- Middleware keamanan

### 3️⃣ Business Logic
- Perhitungan sistem
- Validasi lanjutan
- Rule dan kebijakan aplikasi

### 4️⃣ Database Interaction
- Insert data
- Read data
- Update data
- Delete data

### 5️⃣ Response Handling
- Success response
- Error response
- HTTP status code

---

## 🔄 Contoh Flowchart Backend (Login API)

1. Backend menerima request login
2. Validasi data request
3. Cari user di database
4. Verifikasi password
5. Jika gagal → kirim error response
6. Jika berhasil:
   - Generate token
   - Simpan log / session
7. Kirim response success ke frontend

---

## 🔐 Keunggulan Flowchart Backend

- Logika sistem lebih aman
- Mengurangi bug kritis
- Mempermudah scaling sistem
- Menjadi acuan implementasi API

---

# 🔗 Keterkaitan Flowchart Frontend & Backend

Flowchart frontend dan backend **harus saling terhubung**, namun memiliki tanggung jawab berbeda.

| Frontend | Backend |
|--------|--------|
| Fokus UI & UX | Fokus logika & data |
| Validasi ringan | Validasi utama |
| Menampilkan response | Menghasilkan response |
| User interaction | System processing |

---

## 🧠 Best Practice

- Buat flowchart sebelum menulis kode
- Pisahkan flowchart frontend dan backend
- Gunakan simbol standar
- Hindari alur terlalu kompleks
- Update flowchart saat sistem berubah

---

## 📎 Kesimpulan

Flowchart frontend menjelaskan **bagaimana pengguna berinteraksi dengan sistem**, sedangkan flowchart backend menjelaskan **bagaimana sistem memproses logika dan data di server**. Keduanya merupakan fondasi penting dalam membangun aplikasi yang stabil, aman, dan scalable.

---

# 🗂️ Entity Relationship Diagram (ERD)

Jika flowchart adalah **cerita tentang bagaimana sistem bekerja**, maka ERD adalah **peta dunia tempat cerita itu terjadi**.  
ERD menjelaskan **siapa saja yang ada di dalam sistem, apa peran mereka, dan bagaimana mereka saling terhubung** melalui data.

---

## 📖 ERD dalam Sudut Pandang Cerita

Bayangkan sebuah aplikasi adalah **sebuah kota digital**.

- **Penduduk kota** → adalah data
- **Bangunan** → adalah tabel database
- **Alamat rumah** → adalah primary key
- **Hubungan keluarga & pekerjaan** → adalah relasi antar tabel

Tanpa ERD, kota ini akan kacau:
- Data duplikat
- Hubungan tidak jelas
- Sulit dikembangkan
- Rentan error

ERD hadir sebagai **arsitek kota**, memastikan semua tertata rapi sejak awal.

---

## 📌 Apa Itu ERD?

Entity Relationship Diagram (ERD) adalah **diagram visual yang menggambarkan struktur database** beserta hubungan antar tabel di dalam sebuah sistem.

ERD digunakan untuk:
- Merancang database sebelum implementasi
- Memahami relasi data dengan cepat
- Menjaga konsistensi dan integritas data
- Menjadi dokumentasi backend jangka panjang

---

## 🧱 Komponen Utama ERD (Dengan Analogi)

### 🏢 1️⃣ Entity (Tabel)

**Entity** adalah representasi objek utama dalam sistem.  
Dalam analogi kota, entity adalah **bangunan penting**.

Contoh entity:
- `users`
- `products`
- `transactions`
- `orders`

Setiap entity biasanya menjadi **satu tabel database**.

---

### 🧾 2️⃣ Attribute (Kolom)

**Attribute** adalah detail dari sebuah entity.  
Jika entity adalah bangunan, maka attribute adalah **isi di dalamnya**.

Contoh attribute pada entity `users`:
- `id`
- `name`
- `email`
- `password`
- `created_at`

Attribute menjelaskan **karakteristik data** yang disimpan.

---

### 🔑 3️⃣ Primary Key (PK)

Primary Key adalah **identitas unik** sebuah data.  
Dalam dunia nyata, ini seperti **Nomor KTP**.

Contoh:
- `users.id`
- `products.id`

Primary Key memastikan:
- Tidak ada data yang sama
- Data mudah dicari
- Relasi bisa dibangun dengan aman

---

### 🔗 4️⃣ Foreign Key (FK)

Foreign Key adalah **jembatan penghubung antar tabel**.  
Jika Primary Key adalah KTP, maka Foreign Key adalah **referensi KTP di dokumen lain**.

Contoh:
- `transactions.user_id` → mengacu ke `users.id`

Dengan Foreign Key:
- Data saling terhubung
- Relasi menjadi jelas
- Integritas data terjaga

---

## 🔄 Jenis Relasi dalam ERD (Dengan Cerita)

### 1️⃣ One to One (1:1)
Satu data berhubungan dengan satu data lain.

**Analogi**:  
Satu orang → satu KTP

Contoh:
- `users` ↔ `profiles`

---

### 2️⃣ One to Many (1:N)
Satu data bisa memiliki banyak data lain.

**Analogi**:  
Satu orang → banyak transaksi

Contoh:
- `users` → `transactions`

Artinya:
> Satu user bisa melakukan banyak transaksi,  
> tetapi satu transaksi hanya milik satu user.

---

### 3️⃣ Many to Many (M:N)
Banyak data saling terhubung dengan banyak data lain.

**Analogi**:  
Satu murid → banyak mata pelajaran  
Satu mata pelajaran → banyak murid

Biasanya membutuhkan **tabel penghubung (pivot table)**.

Contoh:
- `users`
- `roles`
- `user_roles`

---

## 🧠 Contoh Cerita ERD dalam Sistem Login & Transaksi

Mari kita lihat sistem sederhana:

- User mendaftar → data masuk ke tabel `users`
- User login → sistem mencocokkan `email` dan `password`
- User melakukan transaksi → data masuk ke tabel `transactions`
- Setiap transaksi menyimpan `user_id` sebagai Foreign Key

Di sini ERD memastikan:
- Transaksi tidak mungkin ada tanpa user
- Data user tidak perlu disalin berulang
- Hubungan data tetap konsisten

---

## 🧩 Peran ERD dalam Backend Development

ERD adalah **fondasi backend**.

Tanpa ERD:
- Query jadi rumit
- Data tidak konsisten
- Sistem sulit dikembangkan

Dengan ERD:
- Struktur database jelas
- Query lebih efisien
- Mudah scaling
- Mudah maintenance

---

## 🔗 Hubungan ERD dengan Flowchart

Flowchart dan ERD **tidak bisa dipisahkan**.

| Flowchart | ERD |
|---------|-----|
| Menjelaskan alur proses | Menjelaskan struktur data |
| Fokus ke logika | Fokus ke relasi |
| Bagaimana sistem berjalan | Di mana data disimpan |
| Urutan kejadian | Hubungan antar data |

Flowchart adalah **alur cerita**,  
ERD adalah **dunia tempat cerita itu berlangsung**.

---

## 🧠 Best Practice Membuat ERD

- Buat ERD sebelum coding backend
- Gunakan penamaan tabel yang konsisten
- Hindari data duplikat
- Gunakan relasi yang jelas
- Update ERD setiap perubahan struktur database

---

## 📎 Kesimpulan ERD

ERD membantu developer memahami **siapa berhubungan dengan siapa di dalam sistem**.  
Dengan ERD yang baik, sistem akan:
- Lebih stabil
- Lebih aman
- Mudah dikembangkan
- Mudah dipahami oleh developer baru

---

> Dokumentasi ERD ini dibuat sebagai panduan konseptual dan teknis  
> agar pengembangan sistem berjalan terstruktur dan berkelanjutan.  
>  
> **Dibuat oleh Yeka**

