# Undangan-Melaspas-Memirak
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Undangan Melaspas & Memirak</title>
  <style>
    body, html {
      margin: 0; padding: 0;
      font-family: "Segoe UI", sans-serif;
      background: #f7f7f7;
      color: #333;
      overflow-x: hidden;
    }
    header {
      background: url('hero.jpg') center/cover no-repeat;
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      color: white;
      position: relative;
    }
    header::after {
      content: "";
      position: absolute;
      top:0; left:0; right:0; bottom:0;
      background: rgba(0,0,0,0.4);
    }
    header h1, header h3, header p {
      position: relative;
      z-index: 1;
      animation: fadeIn 2s ease;
    }
    header h1 { font-size: 2.2rem; margin: 0; }
    header h3 { font-size: 1.2rem; margin: 5px 0; }
    .content {
      max-width: 800px;
      margin: auto;
      padding: 20px;
      text-align: center;
    }
    .btn {
      display: inline-block;
      margin: 10px;
      padding: 12px 20px;
      background: #d35400;
      color: #fff;
      text-decoration: none;
      border-radius: 8px;
      font-weight: bold;
      transition: background 0.3s;
    }
    .btn:hover { background: #e67e22; }
    footer {
      text-align: center;
      padding: 20px;
      background: #222;
      color: #fff;
      margin-top: 20px;
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    .guest {
      position: absolute;
      bottom: 10px;
      right: 10px;
      background: rgba(0,0,0,0.6);
      color: #fff;
      padding: 5px 12px;
      border-radius: 6px;
      font-size: 0.9rem;
      z-index: 2;
    }
  </style>
</head>
<body>
  <header>
    <h1>Undangan Upacara<br>Melaspas & Memirak</h1>
    <h3>Senin, 06 Oktober 2025</h3>
    <p>Jam 16:00 - selesai</p>
    <div class="guest" id="guest"></div>
  </header>

  <div class="content">
    <p>
      Atas Rahmat Tuhan Yang Maha Esa,<br>
      kami bermaksud mengundang Anda di acara Kami.<br>
      Merupakan suatu kehormatan dan kebahagiaan bagi kami sekeluarga,<br>
      apabila Bapak/Ibu/Saudara/i berkenan hadir dan memberikan doa restu.
    </p>

    <h2>📍 Lokasi</h2>
    <p>
      Alamat: Rumah Keluarga Besar<br>
      (Silakan isi detail alamat atau link Google Maps di sini)
    </p>
    <a href="https://maps.google.com" target="_blank" class="btn">Lihat Lokasi</a>

    <h2>🎶 Musik Pengiring</h2>
    <audio controls>
      <source src="gus_teja_morning_happiness.mp3" type="audio/mpeg">
      Browser Anda tidak mendukung audio.
    </audio>

    <h2>🤝 Konfirmasi Kehadiran</h2>
    <a href="https://wa.me/?text=Halo%2C+saya+akan+hadir+di+acara+Melaspas+%26+Memirak" target="_blank" class="btn">
      Konfirmasi via WhatsApp
    </a>

    <h2>🔗 Bagikan Undangan</h2>
    <a href="#" onclick="shareWA()" class="btn">Bagikan via WhatsApp</a>

    <p style="margin-top:30px;">
      Besar harapan kami jika Bapak/Ibu/Sahabat/Sdr/i berkenan hadir pada acara ini.<br>
      Atas perhatiannya, terima kasih.
    </p>
  </div>

  <footer>
    <p>© 2025 Keluarga Besar</p>
  </footer>

  <script>
    // Personalisasi tamu via ?kpd=Nama
    const params = new URLSearchParams(window.location.search);
    const guestName = params.get("kpd");
    if(guestName){
      document.getElementById("guest").innerText = "Kepada Yth: " + guestName;
    }

    // Share WhatsApp
    function shareWA(){
      const url = window.location.href;
      const text = "Saya mengundang Anda untuk menghadiri Upacara Melaspas & Memirak pada 06 Oktober 2025. Silakan buka undangan di: " + url;
      window.open("https://wa.me/?text=" + encodeURIComponent(text), "_blank");
    }
  </script>
</body>
</html>
