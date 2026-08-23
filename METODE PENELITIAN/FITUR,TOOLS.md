## Teknologi, Tools, dan Fitur IOTERA

### 1. Platform Pengembangan Website

IOTERA dikembangkan sebagai aplikasi berbasis web agar dapat digunakan melalui browser tanpa memerlukan instalasi aplikasi khusus pada perangkat pengguna.

Teknologi utama yang digunakan:

- **React.js**  
  Digunakan untuk membangun antarmuka pengguna IOTERA, seperti Dashboard, halaman pembuatan proyek, Component Library, AI Idea Input, dan 3D Workspace.

- **Vite**  
  Digunakan sebagai build tool dan development environment untuk menjalankan serta membangun aplikasi React dengan proses pengembangan yang lebih cepat.

- **Node.js**  
  Digunakan sebagai runtime JavaScript untuk menjalankan proses pengembangan dan layanan backend apabila sistem membutuhkan komunikasi dengan AI, database, atau layanan lainnya.

---

### 2. Bahasa Pemrograman

Bahasa pemrograman dan teknologi web yang digunakan dalam pengembangan IOTERA meliputi:

- **JavaScript / TypeScript**  
  Digunakan sebagai bahasa utama untuk mengembangkan logika aplikasi, pengelolaan data proyek, integrasi AI, dan interaksi pada lingkungan 3D.

- **JSX / TSX**  
  Digunakan dalam React untuk membangun komponen antarmuka pengguna secara modular.

- **HTML**  
  Digunakan sebagai struktur dasar halaman aplikasi web.

- **CSS**  
  Digunakan untuk mengatur tampilan, layout, responsivitas, dan desain antarmuka IOTERA.

---

### 3. Platform Visualisasi 3D

Visualisasi 3D merupakan salah satu fitur utama IOTERA karena hasil analisis AI tidak hanya ditampilkan dalam bentuk teks, tetapi diterjemahkan menjadi prototype IoT digital.

Teknologi yang digunakan:

- **Three.js**  
  Digunakan sebagai library utama untuk melakukan rendering objek dan lingkungan 3D melalui browser menggunakan WebGL.

- **React Three Fiber**  
  Digunakan sebagai React renderer untuk Three.js sehingga objek 3D dapat dikelola sebagai komponen React dan lebih mudah diintegrasikan dengan antarmuka IOTERA.

- **Drei**  
  Digunakan sebagai kumpulan helper untuk React Three Fiber, misalnya untuk camera control, loading model, environment, dan kebutuhan interaksi 3D lainnya.

Dalam 3D Workspace, pengguna dapat:

- Melakukan zoom.
- Melakukan rotate.
- Menggeser sudut pandang.
- Memilih komponen.
- Memindahkan komponen.
- Menghapus komponen.
- Menambahkan komponen.
- Menghubungkan komponen menggunakan jumper.
- Melihat rancangan IoT secara tiga dimensi.

---

### 4. Sumber Model 3D

Model komponen IoT tidak dibuat seluruhnya dari awal. Model CAD dapat diperoleh dari:

- **3D ContentCentral**

3D ContentCentral digunakan sebagai salah satu sumber model CAD untuk mikrokontroler, sensor, aktuator, dan komponen elektronik yang dibutuhkan.

Model yang telah dipilih kemudian melalui proses:

`Model CAD → STEP (.step) → Konversi → GLB/GLTF → IOTERA`

Format **STEP** dapat digunakan sebagai sumber model CAD, sedangkan **GLB/GLTF** digunakan sebagai format model yang lebih sesuai untuk ditampilkan pada aplikasi berbasis Three.js.

Model yang telah dikonversi kemudian dimasukkan ke dalam **3D Component Library IOTERA**, sehingga aplikasi tidak perlu mengambil model secara langsung dari 3D ContentCentral setiap kali pengguna membuat proyek.

---

### 5. Component Library

Component Library merupakan kumpulan komponen IoT yang telah disiapkan dalam sistem.

Komponen dibagi menjadi beberapa kategori:

- **Microcontroller**
  - ESP32
  - ESP32-CAM
  - Arduino Uno
  - Arduino Nano

- **Sensor**
  - DHT22
  - HC-SR04
  - Soil Moisture Sensor
  - PIR Sensor
  - LDR
  - MQ-135
  - RFID RC522
  - Load Cell

- **Actuator**
  - Servo Motor
  - Relay
  - Water Pump
  - DC Motor
  - Buzzer
  - LED

- **Connection**
  - Jumper Male-Male
  - Jumper Male-Female
  - Jumper Female-Female

Setiap komponen dapat memiliki informasi berupa:

- Nama komponen.
- Kategori.
- Fungsi.
- Tegangan kerja.
- Informasi pin.
- Kompatibilitas.
- Model 3D.
- Deskripsi komponen.

---

### 6. Artificial Intelligence

Artificial Intelligence digunakan sebagai sistem yang membantu menerjemahkan aspirasi pengguna menjadi kebutuhan teknis proyek IoT.

AI digunakan untuk:

- Memahami ide pengguna.
- Mengidentifikasi tujuan proyek.
- Mengidentifikasi fungsi yang dibutuhkan.
- Menentukan kebutuhan sensor.
- Menentukan kebutuhan aktuator.
- Merekomendasikan mikrokontroler.
- Menyusun rancangan awal proyek.
- Menghubungkan hasil rekomendasi dengan Component Library.

AI tidak digunakan hanya untuk menghasilkan jawaban berbentuk paragraf. Hasil AI dibuat dalam bentuk data terstruktur yang kemudian digunakan oleh aplikasi untuk membentuk prototype 3D.

Alur utamanya:

`Ide → AI Analysis → Component Recommendation → Structured Data → 3D Prototype`

---

### 7. Machine Learning Recommendation

Machine Learning Recommendation digunakan untuk membantu menentukan komponen yang paling sesuai berdasarkan kebutuhan proyek pengguna.

Beberapa parameter yang dapat digunakan antara lain:

- Jenis proyek.
- Fungsi yang dibutuhkan.
- Jenis sensor.
- Jenis aktuator.
- Kebutuhan komunikasi.
- Jumlah pin.
- Tegangan.
- Kompatibilitas mikrokontroler.
- Ketersediaan komponen pada Component Library.

Sistem rekomendasi dibatasi berdasarkan komponen yang tersedia dalam IOTERA agar hasil rekomendasi dapat langsung dihubungkan dengan model 3D yang tersedia.

---

### 8. Speech Recognition

IOTERA menyediakan fitur **Voice Input** untuk membantu pengguna menyampaikan aspirasi melalui suara.

Teknologi yang dapat digunakan:

- **Whisper**
- **Vosk**

Prosesnya:

`Suara Pengguna → Speech Recognition → Teks → AI Analysis → Rekomendasi → Prototype 3D`

Fitur ini bertujuan mempermudah pengguna menyampaikan gagasan tanpa harus mengetahui atau mengetik istilah teknis secara lengkap.

---

### 9. Add Component

Fitur **Add Component** memungkinkan pengguna mengembangkan hasil rancangan yang diberikan AI.

Pengguna dapat:

- Mencari komponen.
- Memilih kategori.
- Menambahkan sensor.
- Menambahkan mikrokontroler.
- Menambahkan aktuator.
- Menghapus komponen.
- Memindahkan posisi komponen.

Komponen yang ditambahkan akan langsung muncul pada 3D Workspace.

---

### 10. Add Jumper

Fitur **Add Jumper** digunakan untuk membuat hubungan antar-komponen secara visual.

Pengguna dapat menentukan:

`Komponen Awal → Pin Awal → Jumper → Pin Tujuan → Komponen Tujuan`

Contoh:

`ESP32 GPIO 34 → Jumper → AO Soil Moisture Sensor`

Kabel kemudian divisualisasikan pada lingkungan 3D sehingga pengguna dapat melihat hubungan antar-komponen secara lebih mudah.

---

### 11. Compatibility dan Connection Validation

IOTERA menyediakan validasi dasar untuk membantu mengurangi kesalahan dalam penyusunan rancangan.

Validasi dapat mencakup:

- Kesesuaian mikrokontroler dan sensor.
- Jenis pin.
- Ketersediaan GPIO.
- Tegangan komponen.
- Koneksi VCC dan GND.
- Konflik penggunaan pin.
- Koneksi antar-komponen.

Apabila terdapat koneksi yang tidak sesuai, sistem dapat memberikan peringatan kepada pengguna sebelum rancangan dilanjutkan.

---

### 12. Project Dashboard

Dashboard digunakan sebagai pusat pengelolaan proyek pengguna.

Fitur yang tersedia meliputi:

- **Create New Project**
- **My Projects**
- Membuka proyek.
- Mengedit proyek.
- Menyimpan proyek.
- Menghapus proyek.
- Melihat informasi proyek.
- Melanjutkan rancangan sebelumnya.

---

### 13. Project Information

Setelah prototype dihasilkan, IOTERA menampilkan informasi pendukung mengenai proyek, antara lain:

- Nama proyek.
- Tujuan proyek.
- Deskripsi proyek.
- Daftar komponen.
- Fungsi setiap komponen.
- Mikrokontroler yang digunakan.
- Sensor dan aktuator.
- Hubungan antar-komponen.
- Arsitektur sistem.
- Prototype 3D.

Dengan demikian, visualisasi 3D tetap dilengkapi informasi teknis yang dapat membantu pengguna memahami rancangan.

---

### 14. Save Project

Fitur **Save Project** digunakan untuk menyimpan hasil rancangan pengguna.

Data yang disimpan dapat meliputi:

- Informasi proyek.
- Daftar komponen.
- Posisi komponen 3D.
- Koneksi jumper.
- Hasil rekomendasi.
- Konfigurasi rancangan.

Pengguna dapat membuka kembali proyek melalui Dashboard untuk melanjutkan proses perancangan.

---

### 15. Export Project

Fitur **Export Project** digunakan untuk menghasilkan keluaran dari rancangan yang telah dibuat.

Output dapat dikembangkan dalam beberapa bentuk:

- Model prototype 3D.
- File GLB/GLTF.
- Daftar komponen.
- Informasi fungsi komponen.
- Informasi koneksi.
- Dokumentasi rancangan proyek.

Hasil tersebut dapat digunakan sebagai referensi awal sebelum pengguna melanjutkan ke tahap pembuatan prototype fisik.

---

### 16. Konsep Utama IOTERA

Keseluruhan teknologi tersebut diintegrasikan dalam satu alur:

`Text / Voice → AI → ML Recommendation → Component Library → 3D Visualization → Add Component → Add Jumper → Validation → Save / Export`

Dengan demikian, **IOTERA (IoT Engineering & Recommendation Assistant)** tidak hanya memberikan rekomendasi proyek dalam bentuk teks, tetapi membantu menerjemahkan aspirasi pengguna menjadi **rancangan awal IoT berbentuk prototype 3D yang dapat dilihat, dimodifikasi, dan dikembangkan secara interaktif**.