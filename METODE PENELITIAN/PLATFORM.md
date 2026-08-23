### Platform dan Pengolahan Model 3D

IOTERA menggunakan **3D ContentCentral** sebagai salah satu platform utama untuk memperoleh model CAD komponen yang digunakan dalam Component Library.

Platform:
- **3D ContentCentral**
- Website: 3dcontentcentral.com

3D ContentCentral menyediakan berbagai model CAD 2D dan 3D, termasuk model komponen yang berasal dari supplier maupun kontribusi pengguna. Model yang telah dipilih kemudian digunakan sebagai aset visual pada sistem IOTERA.

#### Alur Pengambilan Model 3D

Proses pengambilan dan implementasi model dilakukan melalui beberapa tahap:

1. **Login 3D ContentCentral**
   - Pengembang masuk ke akun 3D ContentCentral.
   - Login diperlukan untuk mengakses proses download pada model tertentu.

2. **Search Component**
   - Pengembang mencari komponen yang dibutuhkan dalam IOTERA.
   - Contohnya mikrokontroler, sensor, aktuator, connector, dan komponen pendukung lainnya.

3. **Pemilihan Model**
   - Model dipilih berdasarkan kesesuaian bentuk dan jenis komponen yang tersedia dalam Component Library IOTERA.
   - Model yang digunakan terlebih dahulu dikurasi agar sesuai dengan kebutuhan prototype.

4. **Download STEP**
   - Model CAD diunduh dalam format **STEP (.step/.stp)** apabila format tersebut tersedia pada model yang dipilih.
   - STEP digunakan sebagai format sumber karena umum digunakan untuk pertukaran data model CAD 3D.

5. **Konversi STEP ke GLB**
   - File STEP kemudian dikonversi menjadi format **GLB (.glb)**.
   - Proses konversi diperlukan karena model STEP tidak digunakan secara langsung sebagai format utama rendering pada Three.js/React Three Fiber.

6. **Optimasi Model**
   - Model GLB dapat dioptimalkan untuk mengurangi ukuran file dan kompleksitas geometri agar proses rendering pada browser lebih ringan.
   - Skala, orientasi, dan posisi awal model juga disesuaikan sebelum dimasukkan ke IOTERA.

7. **Import ke IOTERA**
   - File GLB yang telah diproses dimasukkan ke **3D Component Library IOTERA**.
   - Setiap model kemudian dihubungkan dengan data komponen seperti nama, kategori, fungsi, pin, dan kompatibilitas.

8. **Rendering dengan React Three Fiber**
   - React Three Fiber dan Three.js digunakan untuk menampilkan file GLB pada 3D Workspace.
   - Model dapat dipilih, dipindahkan, diputar, ditambahkan, atau dihapus oleh pengguna.

#### Alur Implementasi

`3D ContentCentral → Login → Search Component → Download STEP → Convert STEP to GLB → Optimasi → Component Library → React Three Fiber → 3D Workspace`

#### Contoh

Apabila IOTERA membutuhkan model ESP32:

`Search ESP32 → Download ESP32.step → Convert → esp32.glb → Component Library → AI memilih ESP32 → React memanggil esp32.glb → Model ESP32 tampil di 3D Workspace`

Dengan metode tersebut, **IOTERA tidak mengambil model secara langsung dari 3D ContentCentral setiap kali pengguna membuat proyek**. Model terlebih dahulu dipilih, diunduh, dikonversi, dan dimasukkan ke dalam Component Library IOTERA.

Ketika AI merekomendasikan suatu komponen, sistem cukup mencocokkan hasil rekomendasi dengan model GLB yang telah tersedia.

Contoh struktur data:

ESP32
- ID: MCU001
- Category: Microcontroller
- Model: esp32.glb
- Voltage: 3.3V
- Wi-Fi: Yes
- Bluetooth: Yes
- Pin Data: Available

Dengan demikian:

`Ide User → AI Recommendation → Component ID → GLB Model → 3D Workspace`

Pendekatan ini membuat proses visualisasi lebih terkontrol dan memungkinkan IOTERA menghasilkan prototype IoT 3D berdasarkan komponen yang telah tersedia dalam sistem.