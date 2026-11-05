## Pelatihan AI 101

## Panduan Trainer

Durasi: 60-90 Menit

Peserta:
Pengguna Bisnis Umum, Manajer, Team Leader, dan Knowledge Worker

Tujuan Pembelajaran:

- Memahami bagaimana AI menggunakan konteks dan memory dalam percakapan
- Memahami keterbatasan memory AI
- Mempelajari Framework Prompting:
  - Role
  - Goal
  - Constraint
  - Output Format
- Memahami teknik No-Shot, One-Shot, dan Few-Shot Prompting
- Memahami bagaimana prompt yang lebih baik menghasilkan output yang lebih baik

---

# Latihan 0: Memahami Memory dalam Percakapan

## Pengantar Trainer

Banyak pengguna menganggap setiap prompt diproses secara terpisah.

Pada kenyataannya, AI dapat menggunakan informasi yang telah diberikan sebelumnya dalam percakapan sebagai konteks untuk menjawab pertanyaan berikutnya.

Konsep ini sering disebut sebagai:

- Conversation Context
- Context Window
- Chat Memory (dalam satu percakapan)

Mari kita lihat bagaimana hal ini bekerja.

---

### Langkah 0A – Berikan Konteks

#### Prompt

Ini adalah catatan rapat saya. Ingat informasi ini untuk percakapan kita.

Proyek: Revamp Aplikasi Mobile Pelanggan

Proyek saat ini telah selesai 80%.

Desain ulang UI aplikasi mobile telah selesai dan disetujui oleh pengguna bisnis.

Tim pengembang melaporkan bahwa integrasi API memakan waktu lebih lama dari yang diharapkan karena ketergantungan pada sistem CRM lama.

Untuk menghindari keterlambatan jadwal proyek secara keseluruhan, manajemen menyetujui perekrutan dua pengembang eksternal selama satu bulan.

Manajer proyek meminta tinjauan progres mingguan hingga pekerjaan integrasi selesai.

Tim sepakat untuk menunda permintaan fitur baru hingga setelah go-live produksi.

Target tanggal go-live tetap 15 Desember.

#### Respons yang Diharapkan

Baik. Saya akan mengingat catatan rapat ini selama percakapan berlangsung dan menggunakannya sebagai konteks untuk permintaan berikutnya.

---

### Langkah 0B – Ajukan Pertanyaan Lanjutan

#### Prompt

Apa risiko terbesar dalam proyek ini?

#### Hasil yang Diharapkan

Risiko terbesar proyek ini adalah keterlambatan integrasi API yang disebabkan oleh ketergantungan pada sistem CRM lama.

Ketergantungan ini berpotensi memengaruhi jadwal proyek dan mengancam target go-live tanggal 15 Desember apabila aktivitas integrasi memerlukan waktu lebih lama dari yang direncanakan.

#### Diskusi Trainer

Tanyakan kepada peserta:

Bagaimana AI mengetahui adanya keterlambatan integrasi API?

Jawaban:

Karena informasi tersebut telah dibagikan sebelumnya dalam percakapan.

---

### Langkah 0C – Ajukan Pertanyaan Lain

#### Prompt

Keputusan manajemen apa saja yang telah disetujui?

#### Hasil yang Diharapkan

Manajemen menyetujui:

- Merekrut dua pengembang eksternal selama satu bulan.
- Menunda permintaan fitur baru hingga setelah go-live.
- Melakukan review progres mingguan.

#### Diskusi Trainer

Perhatikan:

Prompt hanya berisi sebuah pertanyaan.

Catatan rapat tidak diulang kembali.

AI menggunakan konteks yang telah diberikan sebelumnya.

---

### Langkah 0D – Meminta Output yang Berbeda

#### Prompt

Buat pembaruan eksekutif dalam satu paragraf berdasarkan diskusi proyek kita.

#### Hasil yang Diharapkan

Proyek Revamp Aplikasi Mobile Pelanggan telah mencapai 80% penyelesaian dan masih berada pada jalur yang sesuai untuk target go-live tanggal 15 Desember. Manajemen telah menyetujui penambahan sumber daya pengembang eksternal untuk membantu mengatasi keterlambatan integrasi API yang disebabkan oleh ketergantungan pada sistem CRM lama. Review progres mingguan akan dilaksanakan hingga pekerjaan integrasi selesai, dan seluruh permintaan fitur baru ditunda hingga setelah implementasi produksi.

#### Diskusi Trainer

Tanyakan:

Apakah kita memberikan catatan rapat tersebut lagi?

Jawaban:

Tidak.

AI menggunakan kembali informasi yang telah diberikan sebelumnya.

---

## Poin Penting

### Conversation Memory / Context

AI dapat menggunakan informasi yang diberikan sebelumnya dalam percakapan.

Semakin banyak konteks yang relevan

=

Semakin baik jawabannya.

---

# Penting: Memory Memiliki Batasan

## Pertanyaan Trainer

Tanyakan kepada peserta:

Jika AI mengingat catatan rapat, apakah itu berarti AI mengingat semuanya selamanya?

Kebanyakan peserta akan menjawab:

Ya.

Ini merupakan kesalahpahaman yang umum terjadi.

---

## Analogi Papan Tulis

Jelaskan:

Bayangkan memory AI seperti sebuah papan tulis.

Saat informasi baru terus ditambahkan, papan tulis akan semakin penuh.

Pada akhirnya informasi lama dapat:

- Menjadi kurang penting
- Diringkas
- Tidak lagi dipertimbangkan dalam konteks

---

## Skenario Demonstrasi

Misalkan percakapan berlanjut dengan:

- Ratusan pesan
- Banyak laporan
- Topik yang tidak terkait
- Proyek-proyek baru

Kemudian Anda bertanya:

Apa target tanggal go-live proyek ini?

Kemungkinan hasil:

✅ AI masih mengingat

atau

⚠️ AI memerlukan informasi tersebut kembali

---

## Praktik Terbaik

### Lebih Baik

Berdasarkan catatan rapat yang telah kita diskusikan sebelumnya mengenai proyek Revamp Aplikasi Mobile Pelanggan, apa risiko utamanya?

### Lebih Baik Lagi

Konteks Rapat:

Proyek: Revamp Aplikasi Mobile Pelanggan

Tanggal Go-Live: 15 Desember

Status Saat Ini: 80% selesai

Apa risiko utamanya?

---

## Poin Diskusi Trainer

AI dapat mengingat konteks,

namun AI bukanlah database.

Semakin penting suatu informasi,

semakin disarankan untuk menyediakannya kembali.

---

# Latihan 1: Role, Goal, Constraint & Output Format

## Pengantar Trainer

Prompt engineering pada dasarnya adalah memberikan instruksi yang lebih baik kepada AI.

Kita akan menggunakan catatan rapat yang sama dan secara bertahap memperbaiki prompt yang digunakan.

---

## Langkah 1 – Prompt Dasar

#### Prompt

Ringkas catatan rapat ini.

#### Contoh Hasil

Rapat membahas progres proyek Revamp Aplikasi Mobile Pelanggan. Desain ulang UI telah selesai dan disetujui. Integrasi API mengalami keterlambatan karena ketergantungan pada CRM. Manajemen menyetujui perekrutan pengembang eksternal untuk membantu proyek. Tim akan terus memantau progres dan menargetkan go-live pada 15 Desember.

#### Diskusi

Tanyakan:

- Apakah ini bermanfaat?
- Apakah sudah siap untuk eksekutif?
- Apakah strukturnya jelas?

Jawaban Umum:

Belum sepenuhnya.

---

## Langkah 2 – Tambahkan Goal

#### Prompt

Ringkas catatan rapat ini dan identifikasi keputusan penting serta action item.

#### Contoh Hasil

Ringkasan

Proyek Revamp Aplikasi Mobile Pelanggan telah mencapai 80% penyelesaian. Pekerjaan desain ulang UI telah disetujui, namun integrasi API mengalami keterlambatan akibat ketergantungan pada CRM.

Keputusan Penting

- Merekrut dua pengembang eksternal selama satu bulan
- Menunda permintaan fitur baru hingga setelah go-live

Action Item

- Melanjutkan pekerjaan integrasi API
- Menjalankan review proyek mingguan

#### Poin Penting

Goal memberi tahu AI seperti apa hasil yang dianggap berhasil.

---

## Langkah 3 – Tambahkan Role + Goal

#### Prompt

Anda adalah seorang PMO Manager yang berpengalaman.

Ringkas catatan rapat ini.

Soroti:

- Status proyek
- Keputusan penting
- Risiko
- Action item

#### Contoh Hasil

Status Proyek

Proyek telah mencapai 80% penyelesaian dan masih berada pada jalur yang sesuai untuk target go-live tanggal 15 Desember.

Keputusan Penting

- Menyetujui perekrutan dua pengembang eksternal
- Menunda permintaan fitur baru hingga setelah implementasi produksi

Risiko

- Keterlambatan integrasi API yang disebabkan oleh ketergantungan pada sistem CRM lama

Action Item

- Menyelesaikan aktivitas integrasi API
- Melakukan review mingguan dengan manajemen
- Memantau pemanfaatan sumber daya pengembang eksternal

#### Poin Penting

Role mengubah perspektif.

Seorang PMO biasanya fokus pada:

- Status
- Risiko
- Tata Kelola
- Tindakan

---

## Langkah 4 – Tambahkan Constraints

#### Prompt

Anda adalah seorang PMO Manager yang berpengalaman.

Goal:

Buat pembaruan proyek untuk eksekutif.

Constraints:

- Maksimal 80 kata
- Fokus hanya pada keputusan dan risiko
- Gunakan bahasa bisnis yang profesional
- Abaikan detail teknis yang tidak relevan bagi manajemen

#### Contoh Hasil

Pembaruan Eksekutif

Proyek masih berada pada jalur yang sesuai untuk target implementasi 15 Desember. Manajemen telah menyetujui penambahan dua pengembang eksternal untuk mengurangi risiko keterlambatan jadwal. Risiko utama proyek adalah keterlambatan integrasi API yang disebabkan oleh ketergantungan pada sistem yang sudah ada. Permintaan fitur tambahan telah ditunda hingga setelah go-live untuk menjaga komitmen jadwal proyek.

#### Poin Penting

Constraints mengurangi ambiguitas dan menghilangkan informasi yang tidak diperlukan.

---

## Langkah 5 – Tambahkan Output Format

#### Prompt

Anda adalah seorang PMO Manager yang berpengalaman.

Goal:

Buat ringkasan proyek untuk eksekutif.

Constraints:

- Maksimal 80 kata
- Bahasa bisnis yang profesional
- Fokus pada keputusan dan risiko

Output Format:

Status Proyek:
...

Keputusan:
- ...
- ...

Risiko:
- ...

Tindakan:
- ...

#### Contoh Hasil

Status Proyek:

80% selesai dan masih sesuai target implementasi 15 Desember.

Keputusan:

- Menyetujui dua pengembang eksternal
- Menunda permintaan fitur baru hingga setelah go-live

Risiko:

- Keterlambatan integrasi API akibat ketergantungan pada CRM

Tindakan:

- Menjalankan review progres mingguan
- Memantau pencapaian milestone integrasi

#### Poin Penting

Output format membuat hasil lebih mudah digunakan kembali.

Manusia menyukai struktur.

Sistem juga menyukai struktur.

---

# Latihan 2: Masalah yang Sama, Role yang Berbeda

## Skenario

Penjualan sebuah perusahaan ritel turun 15%.

### CFO

#### Prompt

Anda adalah seorang CFO.

Analisis mengapa penjualan turun 15%.

#### Contoh Hasil

Area Fokus:

- Tren pendapatan
- Dampak terhadap profitabilitas
- Peluang pengurangan biaya
- Implikasi terhadap arus kas

### Direktur Pemasaran

#### Prompt

Anda adalah Direktur Pemasaran.

Analisis mengapa penjualan turun 15%.

#### Contoh Hasil

Area Fokus:

- Efektivitas kampanye
- Kesadaran merek
- Akuisisi pelanggan
- Aktivitas kompetitor

### Direktur Penjualan

#### Prompt

Anda adalah Direktur Penjualan.

Analisis mengapa penjualan turun 15%.

#### Contoh Hasil

Area Fokus:

- Pipeline penjualan
- Tingkat konversi
- Kinerja wilayah
- Produktivitas tim penjualan

### Poin Penting

Data yang sama.

Role yang berbeda.

Jawaban yang berbeda.

---

# Latihan 3: No-Shot vs One-Shot vs Few-Shot

## Skenario

Ulasan Pelanggan:

"Pengiriman terlambat, tetapi layanan pelanggan dengan cepat menyelesaikan masalah dan sangat membantu."

### No-Shot

#### Prompt

Klasifikasikan sentimen berikut.

"Pengiriman terlambat, tetapi layanan pelanggan dengan cepat menyelesaikan masalah dan sangat membantu."

#### Respons Umum

Positif

atau

Campuran

atau

Netral

#### Poin Penting

AI harus menebak.

---

### One-Shot

#### Prompt

Contoh:

Ulasan:

"Produk berhenti berfungsi setelah dua hari."

Klasifikasi:

Negatif

Sekarang klasifikasikan:

"Pengiriman terlambat, tetapi layanan pelanggan dengan cepat menyelesaikan masalah dan sangat membantu."

#### Hasil Umum

Negatif

#### Poin Penting

Satu contoh mengajarkan pola.

Namun juga dapat menimbulkan bias.

---

### Few-Shot

#### Prompt

Contoh 1

Ulasan:

"Produk berhenti berfungsi setelah dua hari."

Klasifikasi:

Negatif

Contoh 2

Ulasan:

"Tim dukungan langsung menyelesaikan masalah saya."

Klasifikasi:

Positif

Contoh 3

Ulasan:

"Ruangan bersih tetapi berisik."

Klasifikasi:

Campuran

Sekarang klasifikasikan:

"Pengiriman terlambat, tetapi layanan pelanggan dengan cepat menyelesaikan masalah dan sangat membantu."

#### Hasil Umum

Campuran

#### Poin Penting

Banyak contoh memberikan konteks yang lebih kaya.

Lebih banyak konteks

=

Lebih konsisten hasilnya.

---

# Latihan 4: No-Shot vs One-Shot vs Few-Shot untuk Penulisan

### No-Shot

#### Prompt

Tulis posting Facebook tentang AI.

#### Contoh Hasil

Artificial Intelligence sedang mengubah berbagai industri di seluruh dunia. Banyak organisasi menggunakan AI untuk meningkatkan efisiensi dan mengotomatisasi pekerjaan.

Observasi:

Terlalu generik.

---

### One-Shot

#### Prompt

Contoh:

Cloud computing bukan lagi sekadar keputusan teknologi. Ini adalah strategi bisnis.

Organisasi yang mengadopsi cloud memperoleh kelincahan, skalabilitas, dan inovasi yang lebih cepat.

Tulis posting Facebook tentang AI.

#### Contoh Hasil

Artificial Intelligence bukan lagi teknologi eksperimental. AI kini menjadi kemampuan bisnis yang penting.

Organisasi yang memanfaatkan AI secara efektif akan meningkatkan pengambilan keputusan, produktivitas, dan pengalaman pelanggan.

Observasi:

Gaya penulisan mulai mengikuti contoh.

---

### Few-Shot

#### Prompt

Contoh 1

Cloud computing bukan lagi sekadar keputusan teknologi. Ini adalah strategi bisnis.

Organisasi yang mengadopsi cloud memperoleh kelincahan, skalabilitas, dan inovasi yang lebih cepat.

Contoh 2

Keamanan siber bukan lagi masalah TI. Ini adalah risiko bisnis.

Organisasi yang berinvestasi dalam keamanan siber membangun kepercayaan dan ketahanan.

Contoh 3

Data bukan lagi sekadar hasil sampingan operasional. Data adalah aset strategis.

Organisasi yang memanfaatkan data secara efektif dapat mengambil keputusan lebih cepat dan lebih baik.

Tulis posting Facebook tentang AI.

#### Contoh Hasil

Artificial Intelligence bukan lagi teknologi masa depan. AI sedang menjadi keunggulan kompetitif.

Organisasi yang berhasil mengadopsi AI akan memberdayakan karyawan, meningkatkan kualitas keputusan, dan membuka peluang bisnis baru.

Pertanyaannya bukan lagi apakah AI akan memengaruhi bisnis Anda.

Pertanyaannya adalah apakah organisasi Anda sudah siap.

#### Poin Penting

Few-shot mengajarkan:

- Struktur
- Nada bahasa
- Gaya penulisan
- Pola

---

# Tantangan Akhir Peserta

#### Prompt Lemah

Buat laporan status proyek.

#### Contoh Prompt yang Ditingkatkan

Anda adalah seorang PMO Manager yang berpengalaman.

Goal:

Buat laporan status proyek mingguan untuk eksekutif.

Constraints:

- Maksimal 150 kata
- Gunakan bahasa bisnis
- Fokus pada risiko dan hambatan
- Sertakan status kesehatan proyek

Output Format:

Proyek:
...

Status:
Hijau / Kuning / Merah

Pencapaian:
- ...

Risiko:
- ...

Tindakan Selanjutnya:
- ...

---

# Ringkasan Pelatihan

Conversation Memory
→ Menggunakan konteks sebelumnya

Memory Limits
→ Informasi penting mungkin perlu diberikan kembali

Role
→ AI harus berperan sebagai siapa?

Goal
→ Apa yang harus dicapai AI?

Constraint
→ Aturan apa yang harus diikuti AI?

Output Format
→ Bagaimana AI harus memberikan jawaban?

No-Shot
→ Tanpa contoh

One-Shot
→ Satu contoh

Few-Shot
→ Beberapa contoh

Prompt Buruk

=

AI Harus Menebak

Prompt Baik

=

AI Mengikuti Instruksi

Lebih Banyak Konteks

=

Hasil yang Lebih Konsisten dan Lebih Dapat Diprediksi
