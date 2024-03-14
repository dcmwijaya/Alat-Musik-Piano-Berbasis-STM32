[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?style=flat)](https://github.com/ellerbrock/open-source-badges/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?logo=github&color=%23F7DF1E)](https://opensource.org/licenses/MIT)
![GitHub last commit](https://img.shields.io/github/last-commit/devancakra/Alat-Musik-Piano-Berbasis-STM32)
![Project](https://img.shields.io/badge/Project-STM32-light.svg?style=flat&logo=arduino&logoColor=white&color=%23F7DF1E)

# Alat-Musik-Piano-Berbasis-STM32
<strong>Proyek Tunggal: Alat Musik Piano Berbasis STM32</strong><br><br>
Segera Hadir...

<br><br>

## Kebutuhan Proyek
| Bagian | Deskripsi |
| --- | --- |
| Papan Pengembangan | STM32F103C8T6 |
| Editor Kode | Arduino IDE |
| Alat Pemrogram | ST-Link/V2 |
| Driver | ST-Link |
| Protokol Komunikasi | Universal Asynchronous Receiver-Transmitter (UART) |
| Dukungan Aplikasi | STM32CubeProgrammer |
| Bahasa Pemrograman | C/C++ |
| Arduino Library | • SoftwareSerial (bawaan)<br>• DFRobotDFPlayerMini |
| Aktuator | Speaker |
| Komponen Lainnya | • Kabel jumper (1 set)<br>• DF-Player Mini MP3-TF16P (x1)<br>• Micro SD card: SanDisk (x1)<br>• Breadboard (x1)<br>• Resistor (x1)<br>• Kapasitor elektrolit (x1)<br>• Tombol tekan 12 x 12 mm (x8) |

<br><br>

## Unduh & Instal
1. Arduino IDE

   ```
   https://www.arduino.cc/en/software
   ```
<br>

2. ST-Link Driver

   ```
   https://bit.ly/STLink_Driver
   ```
<br>

3. STM32CubeProgrammer
   
   ```
   https://bit.ly/STM32_Cube_Programmer
   ```
   
<br><br>

## Rancangan Proyek
<table>
<tr>
<th width="420">Diagram Blok</th>
<th width="420">Diagram Ilustrasi</th>
</tr>
<tr>
<td><img src="" alt="Block-Diagram"></td>
<td><img src="" alt="Pictorial-Diagram"></td>
</tr>
</table>
<table>
<tr>
<th width="840">Pengkabelan</th>
</tr>
<tr>
<td><img src="" alt="Wiring"></td>
</tr>
</table>

<br><br>

## Pengetahuan Dasar
Pada dasarnya, suatu perangkat itu dapat dikomunikasikan dengan perangkat lain baik secara nirkabel maupun dengan kabel. Komunikasi antar perangkat keras yang umum digunakan salah satunya adalah ``` Komunikasi Serial ```. Dapat diketahui bersama bahwa ``` Komunikasi Serial ``` ini ada tiga jenis, yaitu meliputi: ``` UART (Universal Asynchronous Receiver-Transmitter) ```, ``` SPI (Serial Peripheral Interface) ```, dan ``` I2C (Inter Integrated Circuit) ```. Ada dua macam ``` Komunikasi Serial UART ```, yaitu ``` Hardware Serial ``` dan ``` Software Serial ```.  ``` Komunikasi Hardware Serial ``` dapat dilakukan dengan cara menghubungkan pin ``` TX ``` dan pin ``` RX ``` secara ``` menyilang ``` pada masing-masing papan pengembangan, misalnya: ``` RX-TX ```, kemudian ``` TX-RX ```. Pin ``` TX ``` yaitu untuk ``` mengirim data ```, sedangkan pin ``` RX ``` yaitu untuk ``` menerima data ```. ``` Komunikasi Software Serial ``` ini kurang lebih sama dengan ``` Komunikasi Hardware Serial ``` dalam segi pengkabelan, namun ada perbedaan dalam segi pengkodean. Dengan menggunakan ``` Software Serial ``` inilah anda dapat mengatasi masalah keterbatasan pin ``` RX ``` dan ``` TX ``` yang ada di papan pengembangan. Untuk berkomunikasi dengan ``` Software Serial ``` ini cukup mudah, yaitu dengan menggunakan ``` Pin Digital ``` tertentu sebagai ``` pengganti pin TX dan pin RX ```.

<br><br>

## Pengaturan Arduino IDE
1. Buka ``` Arduino IDE ``` terlebih dahulu, kemudian buka proyek ini dengan cara klik ``` File ``` -> ``` Open ``` :

   <table><tr><td width="810">
      
      ``` pianomini_stm32.ino ```

   </td></tr></table><br>
   
2. Isi ``` Url Pengelola Papan Tambahan ``` di Arduino IDE

   <table><tr><td width="810">
      
      Klik ``` File ``` -> ``` Preferences ``` -> masukkan ``` Boards Manager Url ``` dengan menyalin tautan berikut :
      
      ```
      https://github.com/stm32duino/BoardManagerFiles/raw/main/package_stmicroelectronics_index.json
      ```

   </td></tr></table><br>
   
3. ``` Pengaturan Board ``` di Arduino IDE

   <table>
      <tr><th width="810">

      Cara mengatur board ``` STM32F103C8T6 ```
            
      </th></tr>
      <tr><td>
      
      • Klik ``` Tools ``` -> ``` Board ``` -> ``` Boards Manager ``` -> Instal ``` STM32 MCU based boards ```.

      • Kemudian klik ``` Tools ``` -> ``` Board ``` -> ``` STM32 boards groups ``` -> ``` Generic STM32F1 series ```.

      </td></tr>
   </table><br>
   
4. ``` Ubah Nomor Bagian Papan ``` di Arduino IDE

   <table><tr><td width="810">
      
      Klik ``` Tools ``` -> ``` Board part number ``` -> ``` BluePill F103C8 ```

   </td></tr></table><br>
   
5. ``` Ubah Dukungan U(S)ART ``` di Arduino IDE

   <table><tr><td width="810">
      
      Klik ``` Tools ``` -> ``` U(S)ART Support ``` -> ``` Enabled (generic 'Serial') ```

   </td></tr></table><br>

6. ``` Ubah Metode Pengunggahan ``` di Arduino IDE

   <table><tr><td width="810">
      
      Klik ``` Tools ``` -> ``` Upload method ``` -> ``` STM32CubeProgrammer (SWD) ```

   </td></tr></table><br>
   
7. Sebelum mengunggah program, silakan klik: ``` Verify ```.<br><br>

8. Jika tidak ada kesalahan dalam kode program, langkah selanjutnya yaitu menggunakan alat pemrograman ``` STM32 ``` sesuai dengan prosedur. Kemudian klik: ``` Upload ```.<br><br>

9. Jika masih ada masalah saat unggah program, maka coba periksa pada bagian ``` driver ``` / ``` port ``` / ``` alat pemrogram ``` / ``` yang lainnya ```.

<br><br>

## Pengaturan ST-Link/V2
Segera Hadir...

<br><br>

## Memulai
1. Unduh dan ekstrak repositori ini.<br><br>
   
2. Pastikan anda memiliki komponen elektronik yang diperlukan.<br><br>
   
3. Pastikan komponen anda telah dirancang sesuai dengan diagram.<br><br>
    
4. Konfigurasikan perangkat anda menurut pengaturan di atas.<br><br>

5. Selamat menikmati [Selesai].

<br><br>

## Sorotan
<img width="840" src="" alt="pianomini-stm32">

<br><br>

## Apresiasi
Jika anda merasa karya ini bermanfaat, dukunglah karya ini sebagai bentuk apresiasi kepada penulis dengan cara mengeklik tombol ``` ⭐Bintang ```.

<br><br>

## LISENSI
LISENSI MIT - Hak Cipta © 2024 - Devan C. M. Wijaya, S.Kom

Dengan ini diberikan izin tanpa biaya kepada siapa pun yang mendapatkan salinan perangkat lunak ini dan file dokumentasi terkait perangkat lunak untuk menggunakannya tanpa batasan, termasuk namun tidak terbatas pada hak untuk menggunakan, menyalin, memodifikasi, menggabungkan, mempublikasikan, mendistribusikan, mensublisensikan, dan/atau menjual salinan Perangkat Lunak ini, dan mengizinkan orang yang menerima Perangkat Lunak ini untuk dilengkapi dengan persyaratan berikut:

Pemberitahuan hak cipta di atas dan pemberitahuan izin ini harus menyertai semua salinan atau bagian penting dari Perangkat Lunak.

DALAM HAL APAPUN, PENULIS ATAU PEMEGANG HAK CIPTA DI SINI TETAP MEMILIKI HAK KEPEMILIKAN PENUH. PERANGKAT LUNAK INI DISEDIAKAN SEBAGAIMANA ADANYA, TANPA JAMINAN APAPUN, BAIK TERSURAT MAUPUN TERSIRAT, OLEH KARENA ITU JIKA TERJADI KERUSAKAN, KEHILANGAN, ATAU LAINNYA YANG TIMBUL DARI PENGGUNAAN ATAU URUSAN LAIN DALAM PERANGKAT LUNAK INI, PENULIS ATAU PEMEGANG HAK CIPTA TIDAK BERTANGGUNG JAWAB, KARENA PENGGUNAAN PERANGKAT LUNAK INI TIDAK DIPAKSAKAN SAMA SEKALI, SEHINGGA RISIKO ADALAH MILIK ANDA SENDIRI.
