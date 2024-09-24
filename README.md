
# Smart Plantig with Iot - Sky Farming Project

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Repositori ini berisi kode dan dokumentasi untuk proyek "Penanaman Cerdas dengan IoT". Proyek ini bertujuan untuk mengotomatiskan dan memantau kondisi lingkungan dalam sistem penanaman menggunakan perangkat IoT dan sensor.

## Daftar Isi
- [Ikhtisar Proyek](#ikhtisar-proyek)
- [Fitur](#fitur)
- [Persyaratan Perangkat Keras](#persyaratan-perangkat-keras)
- [Persyaratan Perangkat Lunak](#persyaratan-perangkat-lunak)
- [Instruksi Setup](#instruksi-setup)
- [Penggunaan](#penggunaan)
- [Kontribusi](#kontribusi)
- [Lisensi](#lisensi)

## Ikhtisar Proyek

Proyek Penanaman Cerdas dengan IoT dirancang untuk meningkatkan proses menanam dengan memanfaatkan teknologi IoT. Sistem ini memantau faktor lingkungan penting seperti kelembaban tanah, suhu, dan intensitas cahaya, serta menyiram tanaman secara otomatis saat diperlukan. Data dikumpulkan dari sensor dan dapat diakses melalui dashboard web atau aplikasi mobile.

## Fitur
- **Pemantauan Real-time**: Mengumpulkan data dari sensor secara real-time untuk kelembaban tanah, suhu, kelembaban udara, dan intensitas cahaya.
- **Irigasi Otomatis**: Menyiram tanaman secara otomatis ketika kelembaban tanah berada di bawah ambang batas tertentu.
- **Antarmuka Web dan Mobile**: Melihat data dan mengontrol sistem dari jarak jauh melalui dashboard web atau aplikasi mobile.
- **Peringatan**: Menerima notifikasi saat kondisi di luar kisaran optimal.
- **Logging Data**: Penyimpanan data historis untuk melacak pertumbuhan tanaman dan tren lingkungan.

## Persyaratan Perangkat Keras
Untuk membangun sistem ini, Anda memerlukan komponen perangkat keras berikut:
- Mikrokontroler ESP32/ESP8266
- Sensor kelembaban tanah
- Sensor suhu dan kelembaban DHT11/DHT22
- Sensor cahaya (misalnya, LDR atau BH1750)
- Pompa air dengan modul relay
- Kabel jumper dan breadboard
- Catu daya
- Pot tanaman dan tanah

## Persyaratan Perangkat Lunak
- Arduino IDE (untuk pemrograman ESP32/ESP8266)
- Library:
  - `WiFi.h`
  - `DHT.h`
  - `Adafruit_Sensor.h`
  - `PubSubClient.h` (untuk MQTT)
  - `ThingSpeak.h` (opsional, untuk penyimpanan data)
- Server web atau platform cloud (misalnya, Blynk, ThingSpeak, atau dashboard web khusus)

## Instruksi Setup

1. **Clone Repositori**:
   ```bash
   git clone https://github.com/d-khalang/Smart-planting-with-IoT.git
   cd Smart-planting-with-IoT
   ```

2. **Pasang Perangkat Keras**:
   Sambungkan sensor dan pompa air ke ESP32/ESP8266 sesuai dengan diagram skematik yang disediakan.

3. **Instal Library Arduino**:
   Instal library yang diperlukan melalui manajer library Arduino IDE, atau unduh dan tambahkan secara manual ke folder library Arduino.

4. **Konfigurasi Kode**:
   - Buka file `.ino` di Arduino IDE.
   - Perbarui kredensial Wi-Fi dalam kode:
     ```cpp
     const char* ssid = "your-SSID";
     const char* password = "your-PASSWORD";
     ```

   - Jika Anda menggunakan broker MQTT atau platform cloud seperti ThingSpeak, konfigurasikan kredensial yang diperlukan.

5. **Unggah Kode**:
   Kompilasi dan unggah kode ke papan ESP32/ESP8266 menggunakan Arduino IDE.

6. **Pantau Sistem**:
   Setelah sistem berjalan, Anda dapat memantau data di dashboard web atau aplikasi mobile dan mengontrol sistem penyiraman.

## Penggunaan

- Akses dashboard web/aplikasi mobile untuk melihat data sensor secara real-time dan mengontrol sistem penyiraman.
- Sistem akan secara otomatis menyiram tanaman saat kelembaban tanah rendah.
- Anda dapat mengontrol pompa air secara manual jika diperlukan melalui dashboard.
- Peringatan akan dikirim jika suhu, kelembaban, atau tingkat cahaya berada di luar kisaran optimal untuk pertumbuhan tanaman.

## Kontribusi

Kontribusi sangat diterima! Jika Anda ingin berkontribusi pada proyek ini, ikuti langkah-langkah berikut:
1. Fork repositori ini.
2. Buat branch fitur (`git checkout -b feature/FiturLuarBiasa`).
3. Commit perubahan Anda (`git commit -m 'Tambahkan FiturLuarBiasa'`).
4. Push ke branch (`git push origin feature/FiturLuarBiasa`).
5. Buka Pull Request.

## Lisensi

Proyek ini dilisensikan di bawah Lisensi MIT. Lihat file [LICENSE](LICENSE) untuk detail lebih lanjut.
