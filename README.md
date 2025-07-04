# Blockchain_Smart-Frementation
Sistem ini akan memanfaatkan teknologi sensor suhu dan kelembapan yang terintegrasi dengan perangkat lunak berbasis web3, yang memungkinkan pemantauan jarak jauh dan pengambilan keputusan yang lebih baik dalam pengelolaan proses fermentasi.

![image](https://github.com/user-attachments/assets/50d94857-4990-4e52-bcb1-d92adabaf7ba)


🔬 Sistem Kontrol & Pemantauan Fermentasi Presisi

Proyek ini adalah solusi lengkap untuk mengotomatisasi dan memantau proses fermentasi. Dibuat untuk memastikan setiap batch menghasilkan kualitas yang konsisten dengan menciptakan lingkungan yang sempurna. Ucapkan selamat tinggal pada tebak-tebakan suhu dan kelembapan!


✨ Fitur Unggulan

Kondisi Live:data suhu dan kelembapan langsung dari ruang fermentasi Anda, detik demi detik. Tak ada lagi yang terlewat.

Kontrol Otomatis: Sistem secara otomatis menyesuaikan pemanas atau pendingin untuk menjaga kondisi ideal yang sudah Anda tentukan. Biarkan mesin yang bekerja, Anda tinggal menikmati hasilnya.

Dashboard Web: Visualisasikan data historis melalui grafik yang mudah dibaca. Lakukan analisis, konfigurasikan parameter, dan kendalikan seluruh sistem dari satu tempat.

Integritas Data Blockchain: Setiap data yang tercatat. Teknologi blockchain digunakan untuk memastikan data tidak dapat dimanipulasi, memberikan lapisan kepercayaan ekstra pada hasil pemantauan Anda.

Pencatatan Data Andal: Seluruh riwayat data sensor disimpan secara efisien di InfluxDB, sebuah database yang dirancang khusus untuk data deret waktu (time-series).


![image](https://github.com/user-attachments/assets/7801892f-1fcc-4299-9ad8-dc28efbf627f)


🚀 Tumpukan Teknologi (Tech Stack)

Backend (Modbus Client): Rust dengan Tokio sebagai runtime asinkron. Dipilih karena performanya yang luar biasa, keamanan memori, dan kemampuannya menangani I/O secara efisien.

Aplikasi Desktop (GUI): Python dengan Tkinter untuk antarmuka yang simpel dan Matplotlib untuk plotting grafik data dari InfluxDB.

Database: InfluxDB sebagai gudang utama untuk semua data sensor suhu dan kelembapan.

Keamanan Data: Implementasi Blockchain untuk memastikan jejak data yang tidak bisa diubah (immutable).

![image](https://github.com/user-attachments/assets/3d4aa935-3cff-434f-834d-8e74ab2c7084)


⚙️ Bagaimana Cara Kerjanya?

Akuisisi Data: Sensor di lapangan berkomunikasi melalui protokol Modbus RTU. Aplikasi Rust bertugas membaca data suhu dan kelembapan secara berkala.

Pengiriman ke Server: Data yang telah dibaca kemudian dikirimkan ke server pusat melalui koneksi TCP yang stabil.

Penyimpanan & Verifikasi: Server menyimpan data mentah ke InfluxDB. Secara bersamaan, hash dari data tersebut dicatatkan ke dalam blockchain untuk verifikasi di kemudian hari.

Visualisasi & Kontrol: Pengguna dapat mengakses dashboard web untuk melihat grafik real-time, menganalisis data historis, dan mengirim perintah kembali ke sistem.


