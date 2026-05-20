# Laporan Hasil Praktikum: Final Project Aplikasi Berbasis Container

## Identitas Mahasiswa

- **Nama:** Ni Ketut Ari Trisna Dewi
- **NIM:** 2415354019
- **Kelas/Rombel:** TRPL C
- **Tanggal Praktikum:** 20 Mei 2026

---

## Teknologi & Tools yang Digunakan

- **Sistem Operasi:** Windows 11
- **Containerization:** Docker & Docker Hub
- **Bahasa Pemrograman / Framework:** Node.js
- **Tools Lain:** VS Code, Git

---

## Langkah-Langkah Praktikum & Dokumentasi

### Langkah 1:  ⁠Pengujian Docker Compose, Volume, Network, Container

Jelaskan secara singkat apa yang dilakukan pada langkah pertama ini. Jika ada kode atau perintah terminal, tulis seperti contoh di bawah:

```bash
# Contoh perintah terminal yang dijalankan
docker build -t app-good .
```

**Dokumentasi/Screenshot:**
![Proses Build Sukses](img/screenshot-langkah1.png)

---

### Langkah 2: Pengujian Endpoint -> Request dan Response (Browser, Postman)

Jelaskan proses penamaan ulang _image_ dan proses unggah ke Docker Hub milik Anda.

```bash
docker tag app-good madedianpp/app-good:v1.0
docker push madedianpp/app-good:v1.0
```

**Dokumentasi/Screenshot:**
![Proses Push Berhasil](dokumentasi/push-docker-hub.png)

---

### Langkah 3: Pengujian upload ke Docker Hub

Jelaskan bagaimana cara melakukan verifikasi atau pengujian bahwa praktikum Anda berhasil berjalan.

```bash
docker run -d -p 8080:8080 madedianpp/app-good:v1.0
```

**Dokumentasi/Screenshot:**
<img src="img/screenshot-hasil-browser.png" alt="Aplikasi Berjalan di Browser" width="500">

---

## Kesimpulan

Tuliskan kesimpulan singkat atau kendala yang Anda hadapi beserta solusinya selama melakukan praktikum ini di sini.
