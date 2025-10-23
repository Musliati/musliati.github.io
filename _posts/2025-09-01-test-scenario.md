---
title: "Test Scenario, Test Case, dan Bug Report"
date: 2025-09-01 08:30:00
categories: [Software Testing and Quality Assurance]
tags: [STQA]
image: /assets/images/test-scenario.png
---

# Test Scenario, Test Case, dan Bug Report  

## Pengantar  
**Test Scenario**, **Test Case**, dan **Bug Report** merupakan tiga elemen penting dalam proses pengujian perangkat lunak.  
Ketiganya saling melengkapi untuk memastikan aplikasi berjalan sesuai kebutuhan dan bebas dari kesalahan.

- **Test Scenario** → Gambaran umum mengenai *apa yang akan diuji* untuk memastikan fungsi aplikasi bekerja sesuai kebutuhan.  
- **Test Case** → Langkah-langkah detail pengujian, termasuk input, proses, dan hasil yang diharapkan.  
- **Bug Report** → Laporan formal yang mendokumentasikan kesalahan atau masalah yang ditemukan selama pengujian.

---

## Test Scenario dan Test Case  

### 1. Test Scenario  
Menjawab pertanyaan **“Apa yang harus diuji?”**  
Berfungsi sebagai panduan umum pengujian suatu fitur atau modul.

**Template sederhana Test Scenario:**  
- ID Scenario — Nomor unik skenario pengujian.  
- Deskripsi — Ringkasan pengujian.  
- Modul/Fitur — Komponen sistem yang diuji.  

**Contoh:**  
- TS001: Periksa fungsi slider input berat dan tinggi badan.  
- TS002: Periksa hasil perhitungan dan klasifikasi BMI.  
- TS003: Periksa fungsi penyimpanan history BMI.

---

### 2. Test Case  
Menjawab pertanyaan **“Bagaimana cara melakukan pengujian?”**  
Berisi langkah-langkah detail untuk memverifikasi apakah sistem bekerja dengan benar.

**Template sederhana Test Case:**  
- ID Test Case — Nomor unik test case.  
- Deskripsi — Ringkasan pengujian.  
- Precondition — Kondisi awal sebelum pengujian dimulai.  
- Test Steps — Langkah-langkah detail pengujian.  
- Test Data — Data yang digunakan untuk pengujian.  
- Expected Result — Hasil yang diharapkan.  
- Actual Result — Hasil yang sebenarnya muncul.  
- Status — *Pass* (Lulus) atau *Fail* (Gagal).

---

## Contoh Test Scenario dan Test Case  
### Aplikasi BMI (Body Mass Index)

#### **Scenario TS001 — Slider Input Berat dan Tinggi Badan**
- **TC001:** Verifikasi slider berat menampilkan nilai sesuai posisi (contoh: 60 kg).  
- **TC002:** Verifikasi slider tinggi menampilkan nilai sesuai posisi (contoh: 170 cm).  

**Expected Result:**  
Nilai berat dan tinggi yang ditampilkan sesuai dengan posisi slider.

---

#### **Scenario TS002 — Perhitungan dan Klasifikasi BMI**
- **TC003:** Verifikasi perhitungan BMI sesuai rumus (kg/m²).  
  - Input: Tinggi = 170 cm, Berat = 65 kg.  
  - Hasil: BMI = 22.49.  
- **TC004:** Verifikasi hasil kategori *Underweight*.  
  - Input: Tinggi = 170 cm, Berat = 45 kg.  
  - Hasil: BMI = 15.6, kategori “Underweight”.  
- **TC005:** Verifikasi hasil kategori *Normal*.  
  - Input: Tinggi = 165 cm, Berat = 60 kg.  
  - Hasil: BMI = 22.0, kategori “Normal”.  
- **TC006:** Verifikasi hasil kategori *Overweight*.  
  - Input: Tinggi = 170 cm, Berat = 75 kg.  
  - Hasil: BMI ≈ 25.9, kategori “Overweight”.  
- **TC007:** Verifikasi hasil kategori *Obese*.  
  - Input: Tinggi = 165 cm, Berat = 90 kg.  
  - Hasil: BMI ≈ 33.06, kategori “Obese”.

---

#### **Scenario TS003 — Penyimpanan History BMI**
- **TC008:** Verifikasi penyimpanan hasil BMI terbaru.  
  - Langkah: Simpan hasil BMI.  
  - Hasil: Data tersimpan dan tampil di halaman *History*.  
- **TC009:** Verifikasi penyimpanan banyak data history tanpa kehilangan data lama.  
  - Langkah: Simpan beberapa data BMI berturut-turut.  
  - Hasil: Semua data tersimpan sesuai urutan tanpa ada yang hilang.

---

## Bug Report  

### 1. Pengertian  
**Bug Report** adalah laporan resmi yang menjelaskan kesalahan dalam sistem, termasuk langkah-langkah untuk mereproduksinya dan hasil aktual yang muncul.  
Tujuannya adalah membantu developer memperbaiki masalah dengan cepat dan akurat.

---

### 2. Komponen Bug Report  
- **Bug ID:** Nomor unik laporan bug.  
- **Bug Title:** Judul singkat yang menggambarkan masalah.  
- **Steps to Reproduce:** Langkah-langkah untuk menemukan bug.  
- **Expected Result:** Hasil yang seharusnya terjadi.  
- **Actual Result:** Hasil yang muncul di sistem.  
- **Severity:** Tingkat dampak bug terhadap sistem.  
- **Priority:** Tingkat urgensi perbaikan bug.  
- **Assignee:** Pihak yang bertanggung jawab memperbaiki bug.  
- **Reporter:** Penguji (QA) yang melaporkan bug.  
- **Reported On:** Tanggal pelaporan bug.  
- **Build Number:** Versi aplikasi saat bug ditemukan.  

---

### 3. Tingkatan Severity (Dampak Bug)
- **Low:** Tidak memengaruhi fungsi sistem.  
- **Minor (Medium):** Tidak mengganggu fungsi utama, hanya menyebabkan ketidaknyamanan kecil.  
- **Major (High):** Mengganggu fungsi utama, tetapi sistem masih berjalan.  
- **Critical:** Menyebabkan sistem gagal total atau data rusak.

---

### 4. Tingkatan Priority (Urgensi Perbaikan)
- **P1 – Urgent/Critical:** Harus segera diperbaiki.  
- **P2 – High:** Penting, memengaruhi banyak pengguna.  
- **P3 – Medium:** Dapat diperbaiki di rilis berikutnya.  
- **P4 – Low:** Bug minor atau kosmetik, bisa diperbaiki kapan saja.

---

### 5. Contoh Bug Report  
**Bug ID:** BMI-001  
**Bug Title:** Perhitungan BMI salah saat input berat 60 kg dan tinggi 170 cm  
**Steps to Reproduce:**  
1. Buka aplikasi BMI  
2. Masukkan Berat = 60  
3. Masukkan Tinggi = 170  
4. Klik tombol “Hitung”  
**Expected Result:** BMI = 20.8  
**Actual Result:** BMI = 12.5  
**Severity:** Major (High)  
**Priority:** P2 – High  
**Build Number:** Version 1.0.0  
**Testing Platform:** Android  
**Reporter:** SQA (Software Quality Assurance)

---

## Cara Menghindari Bug  

1. **Pahami Persyaratan**  
   Pastikan seluruh tim memahami kebutuhan sistem secara jelas sebelum pengembangan.  

2. **Lakukan Unit Testing**  
   Uji setiap modul secara terpisah agar bug bisa dideteksi di tahap awal.  

3. **Lakukan Code Review**  
   Minta rekan pengembang meninjau kode untuk mendeteksi kesalahan logika.  

4. **Rancang Test Plan yang Komprehensif**  
   Buat rencana pengujian berdasarkan skenario dan kebutuhan sistem.  

5. **Gunakan Automation Testing**  
   Manfaatkan alat otomatis untuk mendeteksi bug dengan cepat dan efisien.  

6. **Tingkatkan Kolaborasi Tim**  
   Bangun komunikasi yang baik antara tim pengembang, penguji, dan manajer proyek.

---

## Kesimpulan  
Test Scenario, Test Case, dan Bug Report merupakan bagian penting dari proses **Software Testing**.  
Dengan dokumentasi yang jelas dan sistematis, tim pengembang dapat:
- Menemukan bug lebih cepat,  
- Menjaga kualitas aplikasi,  
- Meningkatkan efisiensi waktu, dan  
- Memberikan pengalaman pengguna yang lebih baik.  

---

> 📘 *Disusun oleh Kelompok 4 Sistem Informasi 2023 — Sisy, Ilham, Naufal, Tasdik, Fathan, Kezia, Imam, dan Khalika.*
