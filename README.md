# Sistem Informasi Surat Masuk & Surat Keluar Berbasis Web

Nama : Firman Gustiar
Nim : 220220003
Program Studi : Sistem Informasi  
Universitas Muhammadiyah Banten

---

# **Abstract (English)**

The rapid development of digital technology has significantly influenced administrative activities, especially in correspondence management within organizations. Many institutions still rely on manual processes for handling incoming and outgoing letters, such as handwritten logs or physical archives, which often results in data inaccuracy, document loss, and inefficient workflows. This research aims to design and develop a Web-Based Incoming and Outgoing Mail Management System to support staff, administrators, and leaders in managing documents accurately and efficiently. The system is developed using the Waterfall software development model, including requirement analysis, design, implementation, testing, and maintenance. The resulting system provides digital recording, tracking, verification, disposition, and reporting of organizational correspondence.

**Keywords:** Mail Management System, Incoming Letters, Outgoing Letters, Waterfall Model, Web-Based Information System.

---

# **Abstrak (Indonesia)**

Perkembangan teknologi informasi yang pesat memberikan dampak signifikan pada proses administrasi, khususnya dalam pengelolaan surat masuk dan surat keluar. Banyak instansi masih menggunakan cara manual seperti pencatatan kertas atau pengarsipan fisik, sehingga sering terjadi kesalahan data, kehilangan surat, serta proses disposisi yang lambat. Penelitian ini bertujuan merancang dan membangun Sistem Informasi Surat Masuk dan Surat Keluar Berbasis Web untuk mendukung kegiatan administrasi secara lebih cepat, terstruktur, dan akurat. Pengembangan sistem dilakukan menggunakan metode Waterfall yang mencakup analisis kebutuhan, perancangan, implementasi, pengujian, dan pemeliharaan. Sistem yang dihasilkan mampu mendukung pencatatan surat, proses disposisi, pembuatan surat keluar, verifikasi pimpinan, serta pelaporan arsip secara digital dan terintegrasi.

**Kata kunci:** Surat Masuk, Surat Keluar, Disposisi, Sistem Informasi, Waterfall.

---

# **Pendahuluan**

Administrasi surat menyurat merupakan bagian penting dalam kegiatan lembaga pemerintahan, pendidikan, maupun organisasi swasta. Pengelolaan surat masuk dan surat keluar yang baik akan memengaruhi kelancaran proses komunikasi dan koordinasi antarunit. Namun, banyak instansi masih menggunakan sistem manual, seperti buku agenda, arsip kertas, atau penyimpanan dokumen yang tidak terstruktur.

Beberapa masalah umum yang terjadi:

- Sulit melacak surat
- Surat terselip atau hilang
- Proses disposisi lambat
- Tidak ada jejak digital
- Laporan manual memakan waktu

Oleh karena itu, dibutuhkan **Sistem Informasi Surat Masuk dan Surat Keluar Berbasis Web**.

---

# **1. Metode Penelitian — Waterfall**

![Waterfall Model](waterfall.png)

---

# **2. Use Case Diagram**

```
@startuml
left to right direction

actor Petugas
actor Admin
actor Pimpinan
actor Pengirim

rectangle "Sistem Surat" {
  (Catat Surat Masuk)
  (Buat Disposisi)
  (Buat Surat Keluar)
  (Verifikasi Surat Keluar)
  (Kirim Surat Keluar)
  (Arsipkan Surat)
  (Lihat Laporan)
}
@enduml
```

---

# **3. Class Diagram**

```
@startuml
class Surat {
  - id : UUID
  - tanggal : Date
  - pengirim : String
  - perihal : String
  - isi : String
  - status : String
}
@enduml
```

---

# **4. Design Patterns**

### Factory Method

```
@startuml
abstract class SuratFactory {
  + createSurat(type, data)
}
@enduml
```

### Builder Pattern

```
@startuml
class LaporanBuilder {
  + setJudul()
}
@enduml
```

### Singleton Pattern

```
@startuml
class NotifikasiService <<Singleton>> {
}
@enduml
```

---

# **5. Sequence Diagram**

```
@startuml
actor Petugas
participant Sistem
Petugas -> Sistem : inputSurat()
@enduml
```

---

# **6. Activity Diagram Surat Masuk & Surat Keluar**

(Diisi sesuai UML sebelumnya)

---

# **7. State Machine Diagram**

```
@startuml
[*] --> Terdaftar
Terdaftar --> Didisposisi
Didisposisi --> Arsip
@enduml
```

---

# **8. Evaluasi Desain**

Maintainability: Baik  
Reusability: Baik  
Scalability: Baik

---

# **9. Saran Pengembangan**

- Integrasi WhatsApp Gateway
- Notifikasi otomatis
- Dashboard grafik statistik

---

# **Selesai**
