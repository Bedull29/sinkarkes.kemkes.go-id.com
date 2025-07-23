<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>SINKARKES - Cek Dokumen</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background-color: #f7f7f7;
    }
    header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 10px 20px;
      background: #fff;
      box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    }
    .logo {
      display: flex;
      align-items: center;
    }
    .logo img {
      height: 40px;
      margin-right: 10px;
    }
    nav ul {
      list-style: none;
      display: flex;
      gap: 20px;
    }
    nav ul li a {
      text-decoration: none;
      color: #008080;
      font-weight: bold;
    }
    .search-bar {
      border: 1px solid #ccc;
      border-radius: 20px;
      padding: 5px 10px;
    }
    .container {
      max-width: 600px;
      background: #fff;
      margin: 40px auto;
      padding: 30px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      border-radius: 10px;
    }
    .container h2 {
      color: #008080;
    }
    .form-group {
      margin-bottom: 20px;
    }
    .form-group label {
      display: block;
      margin-bottom: 5px;
      font-weight: bold;
    }
    .form-group input {
      width: 100%;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    .btn {
      background: #008080;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    .result {
      margin-top: 20px;
      padding: 15px;
      border-radius: 5px;
      background: #e6f9f9;
      color: #006666;
      display: none;
    }
    .preview-image {
      text-align: center;
      margin-top: 30px;
    }
    .preview-image img {
      max-width: 100%;
      border: 1px solid #ccc;
      border-radius: 10px;
    }
  </style>
</head>
<body>
  <header>
    <div class="logo">
      <img src="D:\codingan dull\sinkarkes clone\SINKARKES.png" alt="logo">
    </div>
    <nav>
      <ul>
        <li><a href="#">PELAYANAN</a></li>
        <li><a href="#">IHR</a></li>
        <li><a href="#">BERITA</a></li>
        <li><a href="#">PERATURAN</a></li>
        <li><a href="#">PROFIL BALAI KARKES</a></li>
        <li><a href="#">VISI MISI</a></li>
        <li><a href="#">FASKES</a></li>
        <li><a href="#">LOGIN</a></li>
      </ul>
    </nav>
    <input class="search-bar" type="text" placeholder="Search...">
  </header>

  <div class="container">
    <h2>Cek Nomor Dokumen</h2>
    <p>Silakan masukkan nomor dokumen atau sertifikat untuk memastikan keasliannya.</p>
    <div class="form-group">
      <label for="docNumber">Nomor Dokumen:</label>
      <input type="text" id="docNumber" placeholder="Masukkan nomor dokumen...">
    </div>
    <button class="btn" onclick="cekDokumen()">Cek Dokumen</button>
    <div class="result" id="resultBox"></div>

    <div class="preview-image">
      <h3>Contoh Sertifikat:</h3>
      <img src="D:\codingan dull\sinkarkes clone\qadir-sertifikat-preview.jpg" alt="Contoh Sertifikat">
    </div>
  </div>

  <script>
    function cekDokumen() {
      const nomor = document.getElementById('docNumber').value;
      const resultBox = document.getElementById('resultBox');
      
      if (nomor.trim() === '') {
        resultBox.style.display = 'block';
        resultBox.innerText = 'Nomor dokumen tidak boleh kosong.';
        resultBox.style.background = '#ffe6e6';
        resultBox.style.color = '#cc0000';
        return;
      }

      // Simulasi hasil (dummy response)
      resultBox.style.display = 'block';
      resultBox.innerHTML = `<strong>Hasil:</strong> Dokumen dengan nomor <em>${nomor}</em> telah terverifikasi.`;
      resultBox.style.background = '#e6f9f9';
      resultBox.style.color = '#006666';
    }
  </script>
</body>
</html>
