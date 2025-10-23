---
title: "Testing Plan"
date: 2025-09-01 07:30:00
categories: [Software Testing and Quality Assurance]
tags: [STQA]
image: /assets/images/testing-plan.png
---

# Testing Plan  

## Pengantar  
**Testing Plan** atau **Rencana Pengujian** adalah dokumen panduan yang menjelaskan bagaimana proses pengujian perangkat lunak dilakukan.  
Rencana ini mencakup ruang lingkup, strategi/metodologi, sumber daya (tim, alat, data uji), serta jadwal pelaksanaan.  

Fungsi utamanya adalah sebagai **acuan resmi** agar kegiatan pengujian berjalan terarah, konsisten, dan terukur.

---

## Tujuan Testing Plan  
- Memberikan gambaran yang jelas tentang apa yang akan diuji dan bagaimana cara pengujiannya.  
- Menemukan sebanyak mungkin kesalahan sebelum produk dirilis.  
- Menjamin perangkat lunak memenuhi kualitas yang dapat diterima pengguna.  
- Mengoptimalkan waktu, biaya, dan tenaga dalam proses pengujian.  
- Menyediakan dokumentasi sebagai referensi dan bahan evaluasi untuk proyek berikutnya.

---

## Komponen Testing Plan (Berdasarkan IEEE 829-1988)

### 1. **Plan Identifier**
- Menyediakan penanda unik untuk setiap dokumen test plan (misalnya berupa kode atau versi).  
- Berfungsi untuk membedakan test plan antar proyek, memudahkan pengelolaan revisi, dan menjadi referensi ketika terjadi perubahan.

---

### 2. **References**
- Berisi daftar dokumen, standar, atau sumber acuan yang digunakan dalam penyusunan test plan.  
- Memastikan pengujian konsisten dengan dokumen utama proyek.  
- Digunakan untuk menyamakan interpretasi dan menjaga validitas hasil pengujian.

---

### 3. **Introduction**
- Bagian pembuka yang berisi tujuan, ruang lingkup, dan fokus pengujian.  
- Memberikan gambaran umum kepada stakeholder sebelum masuk ke bagian teknis.  
- Menjelaskan hasil atau capaian yang diharapkan dari pengujian.

---

### 4. **Test Items**
- Komponen, fitur, atau modul perangkat lunak yang akan diuji.  
- Menentukan ruang lingkup pengujian dari sisi teknis.

---

### 5. **Software Risk Issues**
- Mengidentifikasi potensi risiko yang mungkin muncul selama proses pengujian.  
- Termasuk di dalamnya:
  - Fitur baru atau kompleks.  
  - Integrasi dengan versi perangkat lunak lain.  
  - Kebutuhan yang tidak jelas atau sulit diuji.  
  - Kesalahpahaman terhadap spesifikasi.  

---

### 6. **Features to be Tested**
- Menjelaskan fitur-fitur atau fungsi perangkat lunak yang akan diuji dari perspektif pengguna.  
- Fokus pada fitur yang memiliki risiko tinggi atau berdampak besar terhadap fungsionalitas utama.

---

### 7. **Features Not to be Tested**
- Menyebutkan fitur yang tidak termasuk dalam cakupan pengujian beserta alasannya.  
- Biasanya fitur yang:
  - Sudah stabil dan sering digunakan.  
  - Tidak dirilis pada versi saat ini.  
- Membantu menentukan batas risiko yang masih dapat diterima.

---

### 8. **Approach (Pendekatan Pengujian)**
- Menjelaskan strategi umum pengujian yang akan digunakan, meliputi:
  - Jenis pengujian: Unit, Integration, System, atau Acceptance Testing.  
  - Metode pengujian: Black-box, White-box, atau Gray-box.  
  - Teknik pengujian: Manual atau Otomatis.  
  - Tujuan pengujian: Validasi fungsionalitas, performa, atau keamanan.

---

### 9. **Item Pass/Fail Criteria**
Menetapkan standar yang digunakan untuk menilai apakah pengujian berhasil atau gagal.  

**Pass Criteria:**  
- Semua test case berjalan sesuai harapan.  
- Tidak ada defect kritis yang ditemukan.  
- Fitur berfungsi sesuai spesifikasi.  

**Fail Criteria:**  
- Satu atau lebih test case gagal.  
- Ditemukan bug kritis yang menghambat fungsionalitas utama.  
- Perilaku sistem tidak sesuai spesifikasi.

---

### 10. **Suspension Criteria & Resumption Requirements**
- **Suspension Criteria:** kondisi di mana pengujian harus dihentikan sementara, biasanya karena adanya bug serius atau sistem tidak stabil.  
- **Resumption Requirements:** kondisi yang harus dipenuhi agar pengujian dapat dilanjutkan kembali setelah penundaan.

---

### 11. **Test Deliverables**
- Dokumen dan artefak yang dihasilkan selama proses pengujian, seperti:  
  - Test Plan  
  - Test Case  
  - Hasil eksekusi  
  - Laporan bug  
  - Test Summary Report  

Semua ini menjadi bukti formal bahwa pengujian telah dilakukan.

---

### 12. **Remaining Test Tasks**
- Daftar pekerjaan yang belum selesai saat laporan status dibuat.  
- Termasuk tugas yang harus diselesaikan sebelum pengujian dinyatakan selesai.

---

### 13. **Environmental Needs**
- Spesifikasi lingkungan pengujian seperti:
  - Perangkat keras (hardware)  
  - Perangkat lunak (software & versinya)  
  - Data uji  
  - Kredensial atau akses pengguna  
  - Pengaturan jaringan dan alat bantu  

Lingkungan ini harus dapat direproduksi agar hasil pengujian valid.

---

### 14. **Responsibilities**
- Menjelaskan pembagian tugas dan tanggung jawab setiap anggota tim pengujian, termasuk:  
  - Siapa yang menulis dan menjalankan test case.  
  - Siapa yang memverifikasi perbaikan.  
  - Siapa yang berwenang mengambil keputusan hasil pengujian.  
- Menetapkan jalur pelaporan dan eskalasi untuk mempercepat penanganan bug.

---

### 15. **Staffing and Training Needs**
- Menentukan peran utama seperti Test Manager, Tester, Developer, dan Support Team.  
- Mengidentifikasi kebutuhan pelatihan singkat atau *cross-training* agar tim siap menjalankan pengujian secara efektif.  

---

### 16. **Schedule**
- Menyusun garis waktu pengujian yang mencakup:  
  - Tanggal mulai dan akhir pengujian.  
  - Sesi *retest* dan *sign-off* rilis.  
  - Jadwal review test case dan milestone penting.  
- Jadwal ini juga memperhitungkan ketergantungan terhadap tim developer.

---

### 17. **Glossary**
- Menyediakan daftar istilah teknis dan singkatan yang digunakan dalam dokumen test plan.  
- Membantu semua pihak memiliki pemahaman yang sama terhadap terminologi yang digunakan.

---

### 18. **Approvals**
- Berisi nama, jabatan, tanda tangan, dan tanggal persetujuan dari pihak terkait.  
- Menandakan bahwa seluruh ruang lingkup, jadwal, dan sumber daya telah disetujui oleh manajemen proyek maupun tim pengujian.

---

## Kesimpulan  
**Testing Plan** berfungsi sebagai panduan resmi dalam proses pengujian perangkat lunak.  
Dengan perencanaan yang matang, tim penguji dapat:
- Menjamin bahwa setiap fitur diuji secara menyeluruh,  
- Mengidentifikasi risiko sejak dini,  
- Mengelola waktu dan sumber daya dengan efisien, dan  
- Memberikan dokumentasi lengkap untuk audit dan peningkatan kualitas di masa depan.  

---

> 📘 *Disusun oleh Kelompok 3 Sistem Informasi 2023 — Alifsa, Rezka, Aipun, Raihan, An Naura, Resky, Roland, dan Chandra.*
