<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Cemre GÜMÜŞ - Bilgisayar Mühendisi</title>
  <style>
    body {
      font-family: 'Times New Roman', Times, serif;
      margin: 0;
      padding: 0;
      background: linear-gradient(to bottom right, #cec6a6, #ebe8db);
      line-height: 1.6;
    }

    .container {
      max-width: 900px;
      margin: 40px auto;
      padding: 15px;
    }

    header {
      display: flex;
      align-items: center;
      gap: 20px;
      background-color: darkslategray;
      color: beige;
      padding: 15px;
      border-radius: 10px;
    }

    header img {
      width: 80px;
      height: 80px;
      border-radius: 50%;
      object-fit: cover;
    }

    section {
      background-color: beige;
      margin-top: 20px;
      padding: 15px;
      border-radius: 10px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }

    h2 {
      color: darkslategray;
      padding: 10px 15px;
      border-radius: 8px;
      display: block;
      margin-top: 10px;
      border-bottom: 2px solid #a9a9a9;
      cursor: pointer;
      transition: background 0.3s, color 0.3s;
    }

    h2:hover {
      color: #000;
      text-decoration: underline;
    }

    a {
      color: black;
      text-decoration: none;
    }

    a:hover {
      text-decoration: underline;
    }

    ul {
      list-style-type: disc;
      padding-left: 20px;
    }

    footer {
      background-color: beige;
      color: #a9a9a9;
      text-align: center;
      padding: 10px;
      margin-top: 40px;
      font-size: 14px;
      border-top-left-radius: 10px;
      border-top-right-radius: 10px;
    }

    #scrollBtn {
      display: none;
      position: fixed;
      bottom: 30px;
      right: 30px;
      padding: 12px 16px;
      border-radius: 50%;
      background: linear-gradient(to right, #3e3e3e, #1a1a1a);
      color: white;
      border: 2px solid white;
      font-size: 20px;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
      cursor: pointer;
      transition: transform 0.3s ease, background 0.3s ease;
    }

    #scrollBtn:hover {
      transform: scale(1.1);
      background: linear-gradient(to right, #5e5e5e, #2a2a2a);
    }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <img src="images/ppm.jpg" alt="Cemre Gümüş Fotoğrafı" />
      <div>
        <h1>Cemre GÜMÜŞ</h1>
        <p>Bilgisayar Mühendisliği Öğrencisi | Yapay Zeka & Veri Bilimi</p>
      </div>
    </header>

    <section>
      <h2 onclick="toggleSection('about')">Hakkımda</h2>
      <div id="about" style="display: none;">
        <p>Merhaba, ben yapay zeka ve veri bilimi alanında kendimi geliştirmekteyim. Aynı zamanda sosyal etkinliklerde aktif rol alarak kişisel gelişimimi ilerletmekteyim. Üniversitemin en büyük kulüplerinden biri olan Bilişim Teknolojileri ve Yazılım Kulübü’nde Başkan olarak görev almaktayım.</p>
      </div>
    </section>

    <section>
      <h2 onclick="toggleSection('experience')">Deneyim</h2>
      <div id="experience" style="display: none;">
        <ul>
          <li><strong>KBÜ - BTK</strong> | Bilişim Teknolojileri ve Yazılım Kulübü (2024 - Halen)</li>
          <li><strong>TEDxKarabük</strong> Etkinlik ve Basın Birimi Sorumlusu (Şubat 2025 - Mart 2025)</li>
        </ul>
      </div>
    </section>

    <section>
      <h2 onclick="toggleSection('education')">Eğitim</h2>
      <div id="education" style="display: none;">
        <ul>
          <li><strong>Karabük Üniversitesi</strong> - Bilgisayar Mühendisliği (2023 - 2027)</li>
          <li><strong>Samsun Anadolu Lisesi</strong> (2018 - 2020)</li>
        </ul>
      </div>
    </section>

    <section>
      <h2 onclick="toggleSection('languages')">Diller</h2>
      <div id="languages" style="display: none;">
        <ul>
          <li>Türkçe (Ana Dil)</li>
          <li>İngilizce (Profesyonel)</li>
          <li>Almanca (Ana Dil)</li>
        </ul>
      </div>
    </section>

    <section>
      <h2 onclick="toggleSection('contact')">İletişim</h2>
      <div id="contact" style="display: none;">
        <ul>
          <li><strong>GitHub:</strong> <a href="https://github.com/cemregumus" target="_blank">github.com/cemregumus</a></li>
          <li><strong>LinkedIn:</strong> <a href="https://www.linkedin.com/in/cemregumus/" target="_blank">linkedin.com/in/cemregumus</a></li>
          <li><strong>Email:</strong> cemreguemues@gmail.com</li>
        </ul>
      </div>
    </section>
  </div>

  <footer>
    <p>&copy; 2025 Cemre Gümüş | Tüm Hakları Saklıdır. </p>
  </footer>

  <button onclick="scrollToTop()" id="scrollBtn" title="Yukarı Çık">↑</button>

  <script>
    function toggleSection(id) {
      const section = document.getElementById(id);
      section.style.display = (section.style.display === "none" || section.style.display === "") ? "block" : "none";
    }

    function scrollToTop() {
      window.scrollTo({ top: 0, behavior: 'smooth' });
    }

    window.onscroll = function () {
      const scrollBtn = document.getElementById("scrollBtn");
      scrollBtn.style.display = (document.documentElement.scrollTop > 100) ? "block" : "none";
    };
  </script>
</body>
</html>
