**Dokumentasi: Aplikasi Scanner Kartu Nama Otomatis**
=====================================================

**1\. Deskripsi**
-----------------

**Scanner Kartu Nama Otomatis** adalah sebuah aplikasi web canggih yang dirancang untuk mengubah proses digitalisasi kartu nama fisik menjadi lebih cepat, akurat, dan efisien. Berbeda dengan scanner tradisional yang hanya melakukan OCR (Optical Character Recognition), aplikasi ini memanfaatkan kemampuan _multimodal_ dari **Google Gemini AI** untuk menganalisis gambar kartu nama secara langsung.

Akses aplikasi ini di [https://scannerkartunama.isparmo.com/](https://scannerkartunama.isparmo.com/)

Aplikasi ini mampu membaca, memahami konteks, dan mengekstrak informasi penting seperti nama, jabatan, perusahaan, nomor telepon, dan email, lalu menyusunnya ke dalam format yang terstruktur. Pengguna kemudian dapat menyimpan data ini dalam format CSV atau secara otomatis menambahkannya ke Google Sheet pribadi mereka.

**2\. Teknologi yang Digunakan**
--------------------------------

Aplikasi ini dibangun menggunakan tumpukan teknologi web modern yang berfokus pada interaksi di sisi klien dan pemanfaatan API canggih.

*   **Frontend:**
    
*   **HTML5:** Untuk struktur dasar halaman web.
    
*   **Tailwind CSS:** Untuk styling yang responsif dan modern, memastikan tampilan optimal di berbagai perangkat.
    
*   **JavaScript (ES6+):** Sebagai otak utama aplikasi, menangani semua logika, interaksi pengguna, dan komunikasi dengan API.
    
*   **Inteligensi Buatan (AI):**
    
*   **Gemini Vision API:** Teknologi inti yang digunakan untuk menganalisis gambar kartu nama secara langsung. Ini memungkinkan aplikasi untuk tidak hanya membaca teks, tetapi juga memahami layout dan konteks untuk mengekstrak data dengan akurasi tinggi.
    
*   **Gemini Text Generation API:** Digunakan dalam fitur "Buat Draf Email" untuk menghasilkan teks email follow-up yang relevan dan profesional.
    
*   **Integrasi & API Browser:**
    
*   **Google Apps Script:** Digunakan sebagai "jembatan" yang aman dan efisien untuk mengirim data dari aplikasi web ke Google Sheet milik pengguna tanpa mengekspos kredensial sensitif.
    
*   **WebRTC (getUserMedia API):** Untuk mengakses kamera perangkat (ponsel atau laptop) secara real-time.
    
*   **File Reader API:** Untuk membaca data gambar yang diunggah oleh pengguna dari perangkat mereka.
    
*   **Fetch API:** Untuk semua komunikasi asinkron dengan Gemini API dan Google Apps Script.
    
*   **Local Storage:** Untuk menyimpan API Key Gemini dan URL Google Apps Script di browser pengguna, sehingga tidak perlu dimasukkan berulang kali.
    

**3\. Fitur-fitur Utama**
-------------------------

1.  **Ekstraksi Data Berbasis AI Vision:**
    

*   Mengirim gambar kartu nama langsung ke Gemini untuk analisis, menghasilkan akurasi yang jauh lebih tinggi dibandingkan metode OCR tradisional.
    
*   Secara otomatis mengidentifikasi dan memisahkan nama, jabatan, perusahaan, email, dan nomor telepon.
    

2.  **Dua Metode Input:**
    

*   **Pindai Langsung:** Menggunakan kamera perangkat untuk mengambil foto kartu nama secara real-time.
    
*   **Unggah Gambar:** Memungkinkan pengguna untuk memilih dan mengunggah file gambar kartu nama yang sudah ada di perangkat mereka.
    

3.  **Opsi Penyimpanan Fleksibel:**
    

*   **Simpan sebagai CSV:** Mengunduh data kontak dalam format .csv yang universal dan dapat dibuka di Microsoft Excel, Google Sheets, atau aplikasi spreadsheet lainnya.
    
*   **Integrasi Google Sheet:** Mengirim data secara otomatis ke baris baru di Google Sheet yang telah ditentukan pengguna, lengkap dengan timestamp.
    

4.  **Asisten Email AI:**
    

*   Setelah data diekstrak, pengguna dapat mengklik tombol untuk secara otomatis menghasilkan draf email follow-up yang profesional dan personal, menggunakan data nama, jabatan, dan perusahaan yang baru saja dipindai.
    

5.  **Setup yang Aman dan Terpandu:**
    

*   **Manajemen API Key:** Aplikasi mengharuskan pengguna memasukkan API Key Gemini mereka sendiri, memastikan penggunaan API berada di bawah kendali pengguna.
    
*   **Panduan Terintegrasi:** Menyediakan panduan pop-up yang jelas dan interaktif untuk membantu pengguna mengatur integrasi Google Sheet untuk pertama kalinya.
    

**4\. Untuk Siapa Aplikasi Ini?**
---------------------------------

Aplikasi ini sangat ideal untuk:

*   **Profesional Sales & Marketing:** Untuk mendigitalisasi _lead_ dari pameran, konferensi, atau pertemuan dengan cepat.
    
*   **Business Developer & Networker:** Siapa saja yang sering bertemu orang baru dan bertukar kartu nama.
    
*   **Event Organizer:** Untuk membantu peserta atau tim internal dalam mengelola kontak yang didapat selama acara.
    
*   **Siapa Saja:** Individu yang ingin merapikan tumpukan kartu nama fisik mereka dan mengubahnya menjadi data digital yang mudah diakses dan dikelola.
    

**5\. Cara Menggunakan**
------------------------

Berikut adalah alur kerja penggunaan aplikasi dari awal hingga akhir.

1.  **Setup Awal (Hanya Sekali):**
    

*   Saat pertama kali membuka aplikasi, Anda akan diminta memasukkan **Gemini API Key**.
    
*   Ikuti petunjuk di layar untuk mengunjungi **Google AI Studio**, membuat API Key baru, lalu salin dan tempel ke dalam aplikasi. API Key ini akan disimpan di browser Anda untuk penggunaan selanjutnya.
    

2.  **Pilih Metode Input:**
    

*   **Opsi A: Pindai dengan Kamera:** Klik "Mulai Pindai", arahkan kamera ke kartu nama, dan klik "Ambil Gambar".
    
*   **Opsi B: Unggah Gambar:** Klik "Unggah Gambar" dan pilih file gambar kartu nama dari perangkat Anda.
    

3.  **Proses AI:**
    

*   Aplikasi akan menampilkan layar pemrosesan saat gambar dikirim ke Gemini untuk dianalisis. Proses ini biasanya memakan waktu beberapa detik.
    

4.  **Verifikasi Hasil:**
    

*   Data yang berhasil diekstrak oleh AI akan ditampilkan dalam sebuah formulir. Periksa kembali keakuratannya dan lakukan koreksi jika diperlukan.
    

5.  **Simpan Data:**
    

*   **Ke Google Sheet:**
    
*   Klik tombol **"Simpan ke Google Sheet"**.
    
*   Jika ini pertama kalinya, sebuah panduan akan muncul. Ikuti 5 langkah di dalamnya untuk menyiapkan Google Sheet dan mendapatkan **URL Web App**.
    
*   Masukkan URL tersebut ke aplikasi. Data akan langsung terkirim. Untuk selanjutnya, Anda tidak perlu mengulang setup ini.
    
*   **Ke File CSV:**
    
*   Klik tombol **"Simpan sebagai CSV"** untuk langsung mengunduh file ke perangkat Anda.
    

6.  **(Opsional) Buat Draf Email:**
    

*   Klik tombol **"✨ Buat Draf Email Follow-up"**.
    
*   Sebuah pop-up akan muncul dengan draf email yang sudah dibuat oleh AI. Anda bisa menyalinnya untuk digunakan di aplikasi email Anda.
