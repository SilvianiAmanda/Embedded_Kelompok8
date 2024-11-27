# Sistem Pengelolaan Air Sisa Wudhu untuk Pembersihan Lingkungan Berbasis Kontrol Otomatis

Proyek ini merupakan sistem berbasis Arduino untuk mendaur ulang air sisa wudhu menjadi sumber air pembersih lingkungan. Sistem ini memantau aliran air, tingkat ketinggian tangki, dan mengontrol pompa serta solenoid valve secara otomatis.

---

## Fitur

### Pengelolaan Air Sisa Wudhu
- Menggunakan sensor aliran air (**flow sensor**) untuk mendeteksi adanya air.
- Menggunakan sensor ultrasonik untuk mengukur ketinggian air di tangki.

### Kontrol Otomatis
- **Pompa air** akan menyala jika terdeteksi aliran air.
- **Solenoid valve** akan aktif ketika tangki penuh, sehingga mencegah kebocoran atau tumpahan.

### Tampilan Real-Time
- Informasi mengenai aliran air dan ketinggian tangki ditampilkan pada layar **LCD I2C**.

### Serial Monitoring
- Data sistem juga ditampilkan melalui **Serial Monitor** untuk keperluan debugging.

---

## Cara Kerja
1. **Deteksi Aliran Air**:
   - Sensor water flow akan menghitung jumlah pulsa untuk menentukan apakah ada aliran air.
   - Jika terdeteksi aliran, pompa akan menyala.

2. **Deteksi Ketinggian Tangki**:
   - Sensor ultrasonik mengukur jarak antara sensor dan permukaan air.
   - Jika jarak kurang dari 7 cm, solenoid valve akan aktif untuk membuka aliran air ke saluran pembuangan.

3. **Tampilan Status**:
   - Status aliran air (`Mengalir` atau `Tidak`) dan tangki (`Penuh` atau `Kosong`) ditampilkan pada layar LCD.

4. **Pemantauan Jarak Jauh**:
   - Semua data juga dikirim ke **Serial Monitor** untuk keperluan pengawasan.
