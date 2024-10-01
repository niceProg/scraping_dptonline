# DPTOnline Scraping

DPTOnline Scraping adalah sebuah proyek yang digunakan untuk mengambil data pemilih dari situs **cekdptonline.kpu.go.id** secara otomatis menggunakan Python. Proyek ini memanfaatkan **Selenium** untuk mengontrol browser secara otomatis dan **Openpyxl** untuk membaca dan memperbarui file Excel.

### Fitur Utama
- Scraping data pemilih menggunakan NIK dari situs cek DPT Online.
- Dukungan otomatisasi dengan Selenium.
- Penggunaan **fake user agent** untuk menghindari deteksi bot.
- Penanganan hasil scraping langsung ke file Excel.

## Persyaratan
- **Python 3.9.20** atau versi di atasnya
- Google Chrome dan ChromeDriver
- Paket Python berikut:
  - `selenium`
  - `openpyxl`
  - `webdriver-manager`
  - `fake-useragent`

## Instalasi

1. **Clone repo ini**:
    ```bash
    git clone https://github.com/niceProg/scraping_dptonline.git
    cd scraping_dptonline
    ```

2. **Install dependencies** menggunakan `pip`:
    ```bash
    pip install -r requirements.txt
    ```

    Jika `requirements.txt` belum tersedia, tambahkan dependencies berikut secara manual:
    ```bash
    pip install selenium openpyxl webdriver-manager fake-useragent
    ```

3. **Setup ChromeDriver**:
   Pastikan Anda memiliki Google Chrome yang terinstall di sistem. Proyek ini akan otomatis mengelola dan menginstall ChromeDriver menggunakan `webdriver-manager`.

## Cara Penggunaan

1. **Siapkan file Excel**:
   - Pastikan Anda memiliki file Excel dengan NIK di kolom **B** mulai dari baris ke-6.
   - Tentukan nama sheet yang akan diproses pada variabel `sheets_to_process`.

2. **Jalankan skrip scraping**:
    - Buka terminal dan jalankan perintah berikut:
    ```bash
    python tools.py
    ```

3. **Hasil**:
   - Data hasil scraping akan ditulis kembali ke file Excel di kolom yang sudah ditentukan, serta akan ada tanda warna merah pada kolom NIK jika data tidak ditemukan atau NIK tidak valid.