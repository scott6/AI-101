# Latihan Pelatihan AI 101
## Prinsip Dasar Prompt Engineering

---

# Latihan 0: Memahami Memori Percakapan

## Tujuan

Pelajari bagaimana AI dapat menggunakan informasi yang telah dibagikan sebelumnya dalam sebuah percakapan.

---

## Langkah 0A – Memberikan Konteks

### Prompt

```text
Ini adalah catatan rapat saya. Ingat informasi ini untuk percakapan kita selanjutnya.

Proyek: Perombakan Aplikasi Mobile Pelanggan

Proyek saat ini sudah selesai 80%.

Desain ulang UI aplikasi mobile telah selesai dan disetujui oleh pengguna bisnis (business users).

Tim pengembang melaporkan bahwa integrasi API memakan waktu lebih lama dari yang diperkirakan karena adanya ketergantungan pada sistem CRM lama (legacy system).

To menghindari penundaan pada lini masa proyek secara keseluruhan, manajemen menyetujui perekrutan dua pengembang eksternal selama satu bulan.

Manajer proyek meminta tinjauan kemajuan mingguan (weekly progress review) hingga pekerjaan integrasi selesai.

Tim sepakat untuk menunda permintaan fitur baru sampai setelah aplikasi resmi dirilis (production go-live).

Target tanggal peluncuran (go-live) tetap pada 15 Desember.
```

---

## Langkah 0B – Mengajukan Pertanyaan Lanjutan

### Prompt

```text
Apa risiko terbesar dalam proyek ini?
```

### Diskusi

- Bagaimana AI bisa mengetahui detail proyek tersebut?
- Mengapa catatan rapat tidak perlu diulang kembali?

---

## Langkah 0C – Mengajukan Pertanyaan Lain

### Prompt

```text
Keputusan manajemen apa saja yang disetujui?
```

### Diskusi

- Informasi apa yang diingat oleh AI?
- Mengapa jawabannya masih tetap relevan?

---

## Langkah 0D – Meminta Format Output yang Berbeda

### Prompt

```text
Buat pembaruan eksekutif (executive update) sebanyak satu paragraf berdasarkan diskusi proyek kita.
```

### Diskusi

- Apakah kita memberikan catatan rapat itu lagi?
- Bagaimana cara AI menghasilkan ringkasan tersebut?

---

# Penting: Memori Memiliki Batasan

## Pertanyaan Diskusi

```text
Jika AI mengingat catatan rapat, apakah itu berarti AI akan mengingat semuanya selamanya?
```

---

## Skenario

Bayangkan percakapan berlanjut dalam waktu yang lama:

- Ratusan pesan
- Berbagai topik berbeda
- Beberapa laporan dokumen
- Proyek-proyek baru

Lama kemudian Anda bertanya:

```text
Berapa target tanggal peluncurannya (go-live date)?
```

### Diskusi

- Apakah AI akan selalu ingat?
- Haruskah informasi penting diberikan kembali?

---

## Praktik Terbaik (Best Practice)

### Lebih Baik

```text
Berdasarkan catatan rapat yang kita diskusikan sebelumnya mengenai
proyek Perombakan Aplikasi Mobile Pelanggan,
apa saja risiko utamanya?
```

### Jauh Lebih Baik

```text
Konteks Rapat:

Proyek: Perombakan Aplikasi Mobile Pelanggan
Tanggal Peluncuran: 15 Desember
Status Saat Ini: Selesai 80%

Apa saja risiko utamanya?
```

---

# Latihan 1: Meningkatkan Prompt dengan Peran, Tujuan, Batasan & Format Output (Role, Goal, Constraint & Output Format)

## Skenario

Gunakan catatan rapat yang sama dari Latihan 0.

---

## Langkah 1

### Prompt

```text
Rangkum catatan rapat ini.
```

### Pertanyaan

- Informasi apa yang hilang?
- Apakah ringkasan ini cocok untuk para eksekutif?
- Peningkatan apa yang akan Anda lakukan?

---

## Langkah 2

### Prompt

```text
Rangkum catatan rapat ini dan identifikasikan keputusan penting serta poin tindakan (action items) yang harus dilakukan.
```

### Pertanyaan

- Bagaimana perbedaan hasil output ini dibandingkan dengan Langkah 1?
- Apa saja yang meningkat?
- Apa yang masih kurang?

---

## Langkah 3

### Prompt

```text
Anda adalah seorang Manajer PMO (Project Management Office) yang berpengalaman.

Rangkum catatan rapat ini.

Soroti:
- Status proyek
- Keputusan penting
- Risiko
- Poin tindakan (action items)
```

### Pertanyaan

- Bagaimana peran (role) memengaruhi jawaban AI?
- Informasi baru apa saja yang muncul?

---

## Langkah 4

### Prompt

```text
Anda adalah seorang Manajer PMO yang berpengalaman.

Tujuan:
Buat pembaruan proyek untuk tingkat eksekutif.

Batasan:
- Maksimal 80 kata.
- Fokus hanya pada keputusan dan risiko.
- Gunakan bahasa bisnis yang profesional.
- Abaikan detail teknis yang tidak relevan bagi manajemen.
```

### Pertanyaan

- Apa yang berubah setelah ditambahkan batasan (constraints)?
- Informasi apa yang hilang/dihilangkan?
- Apakah penghilangan informasi tersebut berdampak baik?

---

## Langkah 5

### Prompt

```text
Anda adalah seorang Manajer PMO yang berpengalaman.

Tujuan:
Buat ringkasan proyek untuk tingkat eksekutif.

Batasan:
- Maksimal 80 kata
- Bahasa bisnis yang profesional
- Fokus pada keputusan dan risiko

Format Output:

Status Proyek:
...

Keputusan:
- ...
- ...

Risiko:
- ...

Tindakan Lanjutan (Actions):
- ...
```

### Pertanyaan

- Bagaimana menentukan format output dapat meningkatkan hasil jawaban AI?
- Apakah format ini lebih mudah dipahami dibandingkan versi-versi sebelumnya?

---

# Latihan 2: Bagaimana Peran (Role) Mengubah Jawaban

## Skenario

Penjualan sebuah perusahaan ritel turun sebesar 15% pada kuartal lalu.

---

## Prompt A

```text
Anda adalah seorang CFO (Chief Financial Officer).

Analisis mengapa penjualan bisa turun sebesar 15%.
```

---

## Prompt B

```text
Anda adalah seorang Direktur Pemasaran (Marketing Director).

Analisis mengapa penjualan bisa turun sebesar 15%.
```

---

## Prompt C

```text
Anda adalah seorang Direktur Penjualan (Sales Director).

Analisis mengapa penjualan bisa turun sebesar 15%.
```

---

## Pertanyaan

- Bagaimana peran memengaruhi analisis jawaban?
- Sudut pandang mana yang paling berguna?
- Apakah menggabungkan berbagai sudut pandang bisa memberikan nilai lebih?

---

# Latihan 3: No-Shot vs One-Shot vs Few-Shot

## Skenario

Klasifikasikan sentimen dari ulasan pelanggan berikut:

```text
Pengirimannya terlambat, tetapi layanan pelanggan menyelesaikan masalah dengan cepat dan sangat membantu.
```

---

## No-Shot

### Prompt

```text
Klasifikasikan sentimen dari ulasan ini.

"Pengirimannya terlambat, tetapi layanan pelanggan menyelesaikan masalah dengan cepat dan sangat membantu."
```

---

## One-Shot

### Prompt

```text
Contoh:

Ulasan:
"Produk berhenti berfungsi setelah dua hari."

Klasifikasi:
Negatif

Sekarang klasifikasikan:

"Pengirimannya terlambat, tetapi layanan pelanggan menyelesaikan masalah dengan cepat dan sangat membantu."
```

---

## Few-Shot

### Prompt

```text
Contoh 1

Ulasan:
"Produk berhenti berfungsi setelah dua hari."

Klasifikasi:
Negatif

Contoh 2

Ulasan:
"Tim bantuan menyelesaikan masalah saya seketika."

Klasifikasi:
Positif

Contoh 3

Ulasan:
"Kamarnya bersih tetapi bising."

Klasifikasi:
Campuran (Mixed)

Sekarang klasifikasikan:

"Pengirimannya terlambat, tetapi layanan pelanggan menyelesaikan masalah dengan cepat dan sangat membantu."
```

---

# Latihan 4: No-Shot vs One-Shot vs Few-Shot untuk Penulisan Konten

---

## No-Shot

### Prompt

```text
Buat sebuah postingan Facebook tentang AI.
```

---

## One-Shot

### Prompt

```text
Contoh:

Komputasi awan (Cloud computing) bukan lagi sekadar keputusan teknologi. Ini adalah strategi bisnis.

Organisasi yang mengadopsi cloud akan mendapatkan kelincahan, skalabilitas, dan inovasi yang lebih cepat.

Buat sebuah postingan Facebook tentang AI.
```

---

## Few-Shot

### Prompt

```text
Contoh 1

Komputasi awan (Cloud computing) bukan lagi sekadar keputusan teknologi. Ini adalah strategi bisnis.

Organisasi yang mengadopsi cloud akan mendapatkan kelincahan, skalabilitas, dan inovasi yang lebih cepat.

Contoh 2

Keamanan siber (Cybersecurity) bukan lagi sekadar masalah IT. Ini adalah risiko bisnis.

Organisasi yang berinvestasi dalam keamanan siber akan membangun kepercayaan dan ketahanan.

Contoh 3

Data bukan lagi sekadar produk sampingan dari operasional. Data adalah aset strategis.

Organisasi yang menggunakan data secara efektif dapat mengambil keputusan dengan lebih cepat dan lebih baik.

Buat sebuah postingan Facebook tentang AI.
```

---

# Tantangan Terakhir (Final Challenge)

Tingkatkan kualitas prompt berikut ini:

```text
Buat laporan status proyek.
```

Persyaratan:

- Tambahkan Peran (Role)
- Tambahkan Tujuan (Goal)
- Tambahkan Batasan (Constraints)
- Tambahkan Format Output (Output Format)

Bersiaplah untuk membagikan prompt hasil peningkatan Anda di depan kelas.
