METODE PENELITIAN

Penelitian ini menggunakan metode Research and Development (R&D)
dengan pendekatan Prototype Development. Metode ini dipilih karena
penelitian berfokus pada pengembangan IOTERA (IoT Engineering &
Recommendation Assistant) sebagai platform berbasis web yang
mengintegrasikan Artificial Intelligence, Machine Learning
Recommendation, Speech Recognition, dan visualisasi 3D untuk membantu
pengguna menerjemahkan ide menjadi rancangan awal proyek IoT.

Pengembangan dilakukan secara bertahap agar fungsi sistem dapat diuji
dan disempurnakan berdasarkan kebutuhan pengguna.

1. Identifikasi Masalah dan Analisis Kebutuhan

Tahap awal dilakukan dengan mengidentifikasi permasalahan pengguna dalam
menerjemahkan ide proyek IoT menjadi rancangan teknis. Selanjutnya
dilakukan analisis kebutuhan sistem yang meliputi:

Input ide melalui teks dan suara.

Analisis kebutuhan proyek menggunakan AI.

Rekomendasi mikrokontroler, sensor, aktuator, dan komponen
pendukung.

Component library sebagai basis komponen yang tersedia.

Visualisasi rancangan dalam bentuk 3D.

Penambahan dan pengaturan komponen.

Penambahan koneksi menggunakan kabel jumper.

Penyimpanan dan pengembangan rancangan proyek.

2. Perancangan Sistem

Pada tahap ini dilakukan perancangan alur kerja IOTERA, struktur
antarmuka pengguna, basis data komponen, serta hubungan antara AI dan
lingkungan visualisasi 3D.

Ide Pengguna
      ↓
Teks / Suara
      ↓
Speech Recognition
      ↓
AI Analysis
      ↓
Component Recommendation
      ↓
IoT Project Blueprint
      ↓
3D Visualization
      ↓
Add / Edit Component
      ↓
Add Jumper
      ↓
Prototype IoT 3D

3. Pengembangan Prototype

Prototype IOTERA dikembangkan dalam bentuk aplikasi berbasis web
menggunakan React sebagai dasar pengembangan antarmuka. Visualisasi
komponen dilakukan menggunakan Three.js/React Three Fiber, sedangkan
model 3D komponen IoT diperoleh dari sumber CAD yang telah dikurasi,
seperti 3D ContentCentral, kemudian disesuaikan ke format yang dapat
digunakan pada lingkungan web.

Pada tahap ini juga dikembangkan component library yang berisi
sejumlah mikrokontroler, sensor, aktuator, dan komponen pendukung.
Pembatasan komponen dilakukan agar rekomendasi AI dan visualisasi 3D
tetap berada dalam cakupan komponen yang tersedia pada sistem.

4. Implementasi Artificial Intelligence dan Speech Recognition

AI digunakan untuk menganalisis ide pengguna dan menerjemahkannya
menjadi kebutuhan teknis proyek IoT. Sistem menghasilkan data
terstruktur berupa jenis proyek, mikrokontroler, sensor, aktuator, serta
komponen yang direkomendasikan.

Speech Recognition digunakan untuk mengubah aspirasi pengguna dalam
bentuk suara menjadi teks sebelum diproses oleh AI.

"Saya ingin membuat penyiram tanaman otomatis"
                    ↓
                AI Analysis
                    ↓
ESP32 + Soil Moisture Sensor + Relay + Water Pump
                    ↓
              Prototype 3D

Dengan demikian, keluaran AI tidak berhenti pada jawaban berbentuk teks,
tetapi digunakan sebagai dasar pembentukan rancangan visual.

5. Implementasi Interactive 3D Workspace

Komponen hasil rekomendasi ditampilkan dalam lingkungan 3D. Pengguna
dapat melakukan zoom, rotate, memilih dan memindahkan komponen,
menambah atau menghapus komponen, serta mengatur posisi komponen.

Fitur Add Component memungkinkan pengguna menambahkan sensor,
aktuator, mikrokontroler, atau komponen lain dari component library.
Fitur Add Jumper digunakan untuk membuat hubungan antar-pin komponen
secara visual sehingga rancangan IoT dapat dikembangkan secara
interaktif.

6. Pengujian Sistem

Prototype IOTERA diuji menggunakan metode Black Box Testing terhadap
fungsi utama, yaitu:

Input teks dan suara.

Analisis serta rekomendasi AI.

Pemanggilan dan visualisasi model 3D.

Fitur Add Component.

Fitur Add Jumper.

Pengaturan komponen.

Penyimpanan proyek.

Selain pengujian fungsional, dilakukan pengujian pengguna. Responden
menggunakan IOTERA untuk membuat rancangan awal proyek IoT, kemudian
memberikan penilaian mengenai kemudahan penggunaan, kemudahan memahami
rekomendasi, manfaat visualisasi 3D, dan kemampuan sistem dalam membantu
menuangkan ide.

7. Evaluasi dan Penyempurnaan

Hasil pengujian dianalisis untuk mengetahui kekurangan pada prototype.
Evaluasi digunakan sebagai dasar penyempurnaan antarmuka, sistem
rekomendasi, component library, visualisasi 3D, dan interaksi pengguna
hingga diperoleh prototype IOTERA yang sesuai dengan tujuan penelitian.

METODE PENGUMPULAN DATA

1. Studi Literatur

Studi literatur dilakukan dengan mempelajari jurnal, artikel ilmiah, dan
sumber relevan mengenai Artificial Intelligence, Internet of Things,
Machine Learning Recommendation, Speech Recognition, visualisasi 3D,
serta pengembangan aplikasi berbasis web.

2. Observasi

Observasi dilakukan untuk mengidentifikasi permasalahan dan kebutuhan
pengguna dalam menerjemahkan ide menjadi rancangan awal proyek IoT.

3. Kuesioner

Kuesioner digunakan pada tahap pengujian pengguna untuk mengetahui
tingkat kemudahan penggunaan, kebermanfaatan, kemudahan memahami
visualisasi, serta kemampuan IOTERA dalam membantu pengguna
mengembangkan gagasan proyek IoT.

ALUR METODE PENELITIAN

Identifikasi Masalah
        ↓
Studi Literatur
        ↓
Analisis Kebutuhan
        ↓
Perancangan Sistem
        ↓
Pengembangan Prototype IOTERA
        ↓
Implementasi AI & Speech Recognition
        ↓
Implementasi 3D Workspace
        ↓
Pengujian Sistem
        ↓
Evaluasi
        ↓
Penyempurnaan Prototype
        ↓
Hasil Akhir IOTERA