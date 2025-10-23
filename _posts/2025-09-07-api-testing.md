---
title: "API Testing"
date: 2025-09-07 08:30:00
categories: [Software Testing and Quality Assurance]
tags: [STQA]
image: /assets/images/api-testing.png
---

# API Testing  

## Pengantar  
**API Testing** adalah proses pengujian yang dilakukan pada **Application Programming Interface (API)** untuk memastikan bahwa:  
- API berfungsi sesuai spesifikasi,  
- Dapat menangani berbagai skenario dengan benar, dan  
- Menghasilkan output yang benar berdasarkan input tertentu.  

Pengujian API berfokus pada **lapisan logika bisnis dan komunikasi antar sistem**, bukan pada antarmuka pengguna (*UI*).  

---

## Tujuan dan Pentingnya API Testing  

1. **Memastikan Kesesuaian Spesifikasi**  
2. **Meningkatkan Keandalan Sistem**  
3. **Menjamin Keamanan API**  
4. **Mengukur Performa API**  
5. **Mendukung Otomatisasi Testing**  
6. **Memastikan Integrasi Sistem Berjalan Lancar**  

---

## Tools untuk API Testing  

### 1. **Postman**  
- Antarmuka yang **user-friendly**.  
- Mendukung berbagai metode HTTP seperti `GET`, `POST`, `PUT`, `DELETE`.  
- Fitur **Collection** dan **Testing Automation**.  
- Mendukung **Otentikasi** dan **Visualisasi Response**.  

### 2. **SOAPUI**  
- Mendukung **SOAP** dan **REST API**.  
- Cocok untuk *enterprise testing*.  
- Dapat melakukan *Functional*, *Security*, dan *Load Testing*.  

---

## Anatomi Request & Response API  

### Request API  
Berisi:  
- HTTP Method  
- URL  
- Headers  
- Body  

**Contoh:**
```http
POST /api/users
Host: api.example.com
Content-Type: application/json

{
  "name": "Musliati",
  "email": "musliati@example.com"
}
```

### Response API  
Berisi:  
- Status Code  
- Headers  
- Body  

**Contoh:**
```json
{
  "status": "success",
  "message": "User created successfully",
  "data": {
    "id": 101,
    "name": "Musliati"
  }
}
```

---

## Praktik Menggunakan Postman  

Langkah-langkah:  
1. Buat *collection*.  
2. Pilih metode HTTP.  
3. Masukkan URL API.  
4. Tambahkan *body* dan klik **Send**.  
5. Lihat hasil *response* dan status code.  

**Contoh API:**  
```http
GET https://reqres.in/api/users?page=2
POST https://reqres.in/api/users
{
  "name": "Frisilia",
  "job": "QA Tester"
}
```

---

## Kesimpulan  
**API Testing** memastikan komunikasi antar sistem berjalan lancar dan aman.  
Alat seperti **Postman** dan **SOAPUI** membantu proses validasi, keamanan, dan otomatisasi pengujian.  

> 📘 *Disusun oleh Kelompok 6 Sistem Informasi 2023 — Frisilia Kiki, Indy Sekar Ayu, Musliati, Nayla Zahra Adelia, Muhammad Rifky Kurniawan, Muhammad Dirga Dian Nugraha, Mohammad Abdul Razaq, dan Nur Wahida.*
