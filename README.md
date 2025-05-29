# Tools Ian7672 Web

Repository ini berisi berbagai tools web termasuk file `check-abi.html` untuk cek ABI perangkat.

## Cara mengakses file `check-abi.html`

File `check-abi.html` bisa diakses lewat:

- **Download langsung dari Releases:**  
  Kunjungi [Releases](https://github.com/Ian7672/tools-ian7672-web/releases) dan cari file `check-abi.html` untuk diunduh.

- **Link Raw GitHub:**  
  https://raw.githubusercontent.com/Ian7672/tools-ian7672-web/refs/heads/main/check-abi.html

  > Catatan: Link raw ini akan menampilkan kode HTML mentah, bukan hasil render halaman web.

- **Render langsung di browser (via halaman web lokal)**  
  Kamu bisa buat file HTML sendiri yang mengambil dan merender file `check-abi.html` secara dinamis.

  Contoh kode:

  ```html
  <!DOCTYPE html>
  <html>
  <head>
    <meta charset="UTF-8" />
    <title>Render check-abi.html dari GitHub</title>
  </head>
  <body>
    <h2>Render isi check-abi.html dari GitHub</h2>
    <div id="content">Memuat...</div>

    <script>
      const url = 'https://raw.githubusercontent.com/Ian7672/tools-ian7672-web/refs/heads/main/check-abi.html';

      fetch(url)
        .then(response => {
          if (!response.ok) {
            throw new Error('Gagal mengambil file: ' + response.status);
          }
          return response.text();
        })
        .then(htmlText => {
          document.getElementById('content').innerHTML = htmlText;
        })
        .catch(err => {
          document.getElementById('content').innerText = 'Error: ' + err.message;
        });
    </script>
  </body>
  </html>
