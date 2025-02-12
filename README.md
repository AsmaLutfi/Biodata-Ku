<html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Multi Page Website</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body {
            font-family: Arial, sans-serif;
            background-color: #A35C7A;
            color: white;
            text-align: center;
            padding: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
        }
        .container {
            background-color: #FFCCE1;
            padding: 50px;
            border-radius: 15px;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.2);
            width: 90%;
            max-width: 600px;
            display: none;
            text-align: center;
        }
        h1, h2 { color: #8E3E63; margin-bottom: 10px; }
        p { color: #8E3E63; font-size: 16px; margin: 5px 0; }
        strong { color: #8E3E63; }
        .image-container {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        img {
            width: 100%;
            max-width: 250px;
            height: auto;
            border-radius: 10px;
            margin: 10px 0;
            border: 3px solid white;
        }
        button {
            background-color: white;
            color: #8E3E63;
            border: none;
            padding: 10px 15px;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            margin-top: 10px;
        }
        button:hover { background-color: #f5f5f5; }
    </style>
</head>
<body>

    <!-- Halaman 1: Welcome -->
    <div class="container" id="page1">
        <h1>Welcome Raiders💫</h1>
        <h3>Enjoy your visit, hope you like it</h3>
        <div class="image-container">
            <img src="Welcome.jpg" alt="Welcome">
            <button onclick="showPage('page2')">Next Page</button>
        </div>
    </div>

    <!-- Halaman 2: Biodata -->
    <div class="container" id="page2">
        <h2>📜Informasi Pribadi</h2>
        <img src="Picture 1.jpeg" alt="Foto Profil">
        <p><strong>🧑 Nama:</strong> Asma Lutfi</p>
        <p><strong>📍 Tempat & tanggal lahir:</strong> Siwalempu, 07 Mei 2005</p>
        <p><strong>🏡 Alamat:</strong> Jl. Lengaru, Palu Timur</p>
        <p><strong>🎮 Hobi:</strong> Gaming and Reading</p>
        <p><strong>🍦 Makanan Favorit:</strong> Es Krim</p>
        <p><strong>🥤 Minuman Favorit:</strong> Susu Strawberry</p>
        <p><strong>🎶 Musik Favorit:</strong> Blessing Cover by TNF</p>
        <button onclick="showPage('page1')">Halaman Utama</button>
        <button onclick="showPage('page3')">Next Page</button>
    </div>

    <!-- Halaman 3: Pendidikan -->
    <div class="container" id="page3">
        <h2>🎓 Pendidikan 👩🏻‍🎓</h2>
        <img src="Universitas Tadulako.jpg" alt="Pendidikan">
        <p><strong>🏩 Universitas:</strong> Tadulako</p>
        <p><strong>🏢 Fakultas:</strong> Teknik</p>
        <p><strong>📚 Program Studi:</strong> S1 Sistem Informasi</p>
        <button onclick="showPage('page2')">Kembali ke Halaman 2</button>
        <button onclick="showPage('page1')">Halaman Utama</button>
    </div>

    <script>
        function showPage(pageId) {
            let pages = document.querySelectorAll('.container');
            pages.forEach(page => page.style.display = 'none');
            document.getElementById(pageId).style.display = 'block';
        }

        // Tampilkan halaman pertama saat pertama kali dibuka
        document.addEventListener("DOMContentLoaded", function() {
            showPage('page1');
        });
    </script>

</body>
</html>
