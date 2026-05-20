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

Pada langkah pertama dilakukan pengujian penggunaan Docker Compose untuk menjalankan aplikasi beserta konfigurasi volume, network, dan container. Pengujian ini bertujuan memastikan seluruh service dapat berjalan dengan baik dan saling terhubung.
```bash
# Contoh perintah terminal yang dijalankan
docker build -t app-good .
```

**Dokumentasi/Screenshot:**
![Proses Build Sukses](img/screenshot-langkah1.png)

---

### Langkah 2: Pengujian Endpoint -> Request dan Response (Browser, Postman)

Pada langkah kedua dilakukan pengujian endpoint aplikasi menggunakan browser maupun Postman. Pengujian ini bertujuan memastikan request dan response dari aplikasi berjalan dengan baik sesuai endpoint yang tersedia.
```bash
docker tag app-good madedianpp/app-good:v1.0
docker push madedianpp/app-good:v1.0
```

**Dokumentasi/Screenshot:**
![Proses Push Berhasil](dokumentasi/push-docker-hub.png)

---

### Langkah 3: Pengujian upload ke Docker Hub

Pada langkah ketiga dilakukan proses penamaan ulang (tagging) image Docker dan upload image ke Docker Hub agar image dapat disimpan secara online dan digunakan kembali di perangkat lain.
```bash
docker run -d -p 8080:8080 madedianpp/app-good:v1.0
```

**Dokumentasi/Screenshot:**
<img src="img/screenshot-hasil-browser.png" alt="Aplikasi Berjalan di Browser" width="500">

---

## Kesimpulan

Berdasarkan praktikum yang telah dilakukan, Docker dapat digunakan untuk mempermudah proses pengelolaan aplikasi melalui container, network, volume, dan Docker Compose. Selain itu, Docker Hub memudahkan proses distribusi image aplikasi agar dapat dijalankan di berbagai perangkat.

Kendala yang sempat dihadapi adalah proses koneksi antar container dan proses upload image yang terkadang gagal akibat koneksi internet atau kesalahan penamaan image. Solusinya adalah memastikan konfigurasi Docker Compose sudah benar serta melakukan pengecekan login Docker Hub sebelum melakukan push image.