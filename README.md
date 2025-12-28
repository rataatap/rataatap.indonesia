<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Rataatap Studio</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg: #0f0f0f;
      --bg-soft: #171717;
      --text: #ffffff;
      --muted: #9ca3af;
      --accent: #e5e7eb;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Inter', sans-serif;
    }

    body {
      background: var(--bg);
      color: var(--text);
      line-height: 1.6;
      scroll-behavior: smooth;
    }

    a { color: inherit; text-decoration: none; }

    header {
      position: fixed; top: 0; left: 0; width: 100%;
      background: rgba(15,15,15,0.8);
      backdrop-filter: blur(10px); z-index: 1000;
    }

    .nav {
      max-width: 1200px; margin: auto; padding: 20px;
      display: flex; justify-content: space-between; align-items: center;
    }

    .logo { font-weight: 600; letter-spacing: 1px; }

    .menu { display: flex; gap: 30px; font-size: 14px; color: var(--muted); }
    .menu a:hover { color: var(--text); }

    .hero {
      height: 100vh; display: flex; align-items: center; justify-content: center;
      text-align: center; padding: 0 20px;
    }

    .hero h1 { font-size: clamp(32px, 5vw, 64px); font-weight: 600; margin-bottom: 20px; }
    .hero p { max-width: 600px; margin: auto; color: var(--muted); }

    section { max-width: 1200px; margin: auto; padding: 120px 20px; }
    .section-title { font-size: 28px; font-weight: 500; margin-bottom: 40px; }

    .grid {
      display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 20px;
    }

    .card {
      background: var(--bg-soft); height: 260px;
      display: flex; align-items: center; justify-content: center;
      color: var(--muted); font-size: 14px;
      border: 1px solid #262626; overflow: hidden; position: relative;
      cursor: pointer;
      transition: transform 0.4s ease, box-shadow 0.4s ease;
    }

    .card:hover {
      transform: translateY(-8px);
      box-shadow: 0 20px 40px rgba(0,0,0,0.4);
    }

    .card::after {
      content: ""; position: absolute; inset: 0;
      background: linear-gradient(180deg, transparent, rgba(0,0,0,0.6));
      opacity: 0; transition: opacity 0.4s ease;
    }

    .card:hover::after { opacity: 1; }

    .about { display: grid; grid-template-columns: 1fr 1fr; gap: 40px; }
    .about p { color: var(--muted); }

    @media (max-width: 768px) { .about { grid-template-columns: 1fr; } }

    footer {
      border-top: 1px solid #262626; padding: 40px 20px;
      text-align: center; color: var(--muted); font-size: 14px;
    }

    /* MODAL TEAM */
    .modal {
      position: fixed; inset: 0; background: rgba(0,0,0,0.6);
      display: none; align-items: center; justify-content: center;
      z-index: 2000;
    }

    .modal-content {
      background: var(--bg-soft);
      padding: 40px; max-width: 420px; width: 90%;
      border: 1px solid #262626;
      text-align: center;
    }

    .modal-content img {
      width: 120px; height: 120px; border-radius: 50%;
      object-fit: cover; margin-bottom: 20px;
    }

    .modal-content h3 { margin-bottom: 8px; font-weight: 500; }
    .modal-content p { font-size: 14px; color: var(--muted); }

    .close-btn {
      margin-top: 24px; font-size: 13px; cursor: pointer; color: var(--accent);
    }
  </style>
</head>
<body>

  <!-- NAVBAR -->
  <header>
    <div class="nav">
      <div class="logo">RATAATAP STUDIO</div>
      <nav class="menu">
        <a href="#projects">Projects</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
      </nav>
    </div>
  </header>

  <!-- HERO -->
  <div class="hero">
    <div>
      <h1>Architecture & Interior Design Studio</h1>
      <p>Studio desain arsitektur dan interior dengan pendekatan modern, simpel, dan fungsional.</p>
    </div>
  </div>

  <!-- PROJECTS -->
<section id="projects">
  <div class="section-title">Popular Design</div>

  <div class="grid">

    <div class="card">
      <img src="rendering-view-fururistic (1).jpeg" alt="Project 01" width="100%">
    </div>

    <div class="card">
      <img src="rendering-view-fururistic (2).jpeg" alt="Project 02" width="100%">
    </div>

    <div class="card">
      <img src="RENDER-CLASIC.jpeg" alt="Project 03" width="100%">
    </div>

    <div class="card">
      <img src="RENDER-MODEREN-MINIMALIS.jpeg" alt="Project 04" width="100%">
    </div>

    <div class="card">
      <img src="RENDER-MODEREN-KONTEMPORER.jpeg" alt="Project 05" width="100%">
    </div>

    <div class="card">
      <img src="RENDER-INDUSTRIAL.jpeg" alt="Project 06" width="100%">
    </div>

  </div>
</section>



  <!-- ABOUT -->
  <section id="about">
    <div class="section-title">About Us</div>
    <div class="about">
      <p>
        Rataatap Studio adalah jasa desain arsitektur dan interior yang berfokus pada visual yang bersih,
        modern, dan kontekstual. Kami menangani desain gambar, konsep, hingga visualisasi 3D.
      </p>
      <p>
        Didirikan pada 11 November 2025, Rataatap bertujuan menghadirkan desain yang efisien,
        realistis, dan siap diwujudkan.
      </p>
    </div>

    <!-- TOGGLE TEAM -->
    <div style="margin-top:60px;">
      <button id="teamToggle" style="background:none;border:1px solid #262626;color:#e5e7eb;padding:14px 28px;cursor:pointer;font-size:14px;">
        Lihat Tim Kami
      </button>
    </div>

    <!-- TEAM SECTION (HIDDEN) -->
    <div id="teamSection" style="display:none;margin-top:60px;">
      <div class="section-title">Our Team</div>
      <div class="grid" style="grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));">

        <div class="card" onclick="openModal('Head Office','Penanggung jawab utama operasional dan arah studio.','images/team1.jpg')" style="height:220px;">
          <div style="text-align:center;">
            <img src="fotozidan.jpg.jpeg" style="width:100px;height:100px;border-radius:50%;object-fit:cover;margin-bottom:12px;">
            <div>Head Office</div>
          </div>
        </div>

        <div class="card" onclick="openModal('Desainer Arsitektural','Mengembangkan konsep desain dan gambar arsitektur.','images/team2.jpg')" style="height:220px;">
          <div style="text-align:center;">
            <img src="fotoilham.jpg.jpeg" style="width:100px;height:100px;border-radius:50%;object-fit:cover;margin-bottom:12px;">
            <div>Desainer Arsitektural</div>
          </div>
        </div>

        <div class="card" onclick="openModal('Civil Engineering','Menangani struktur dan kelayakan teknis bangunan.','images/team3.jpg')" style="height:220px;">
          <div style="text-align:center;">
            <img src="fotoeko.jpg.jpeg" style="width:100px;height:100px;border-radius:50%;object-fit:cover;margin-bottom:12px;">
            <div>Civil Engineering</div>
          </div>
        </div>

        <div class="card" onclick="openModal('Desainer Interior','Mengatur ruang, material, dan estetika interior.','images/team4.jpg')" style="height:220px;">
          <div style="text-align:center;">
            <img src="fotoridwan.jpg.jpeg" style="width:100px;height:100px;border-radius:50%;object-fit:cover;margin-bottom:12px;">
            <div>Desainer Interior</div>
          </div>
        </div>

        <div class="card" onclick="openModal('Konten Creator','Mengelola visual, sosial media, dan branding digital.','images/team5.jpg')" style="height:220px;">
          <div style="text-align:center;">
            <img src="foto-creator.jpg" style="width:100px;height:100px;border-radius:50%;object-fit:cover;margin-bottom:12px;">
            <div>Konten Creator</div>
          </div>
        </div>

      </div>
    </div>
  </section>

  <!-- MODAL -->
  <div id="teamModal" class="modal" onclick="closeModal()">
    <div class="modal-content" onclick="event.stopPropagation()">
      <img id="modalImg" src="" alt="">
      <h3 id="modalTitle"></h3>
      <p id="modalDesc"></p>
      <div class="close-btn" onclick="closeModal()">Tutup</div>
    </div>
  </div>

  <!-- CONTACT -->
  <!-- SERVICES -->
  <section id="services">
    <div class="section-title">Harga & Layanan</div>
    <div class="grid" style="grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));">

      <div class="card" onclick="openService('Jasa Desain Rumah','images/service-rumah.jpg')">
        <div>Jasa Desain Rumah</div>
      </div>

      <div class="card" onclick="openService('Jasa Desain Villa Arsitektural','images/service-villa.jpg')">
        <div>Jasa Desain Villa Arsitektural</div>
      </div>

      <div class="card" onclick="openService('Jasa Desain Interior','images/service-interior.jpg')">
        <div>Jasa Desain Interior</div>
      </div>

      <div class="card" onclick="openService('Jasa Bangunan Lainnya','images/service-lainnya.jpg')">
        <div>Jasa Bangunan Lainnya</div>
      </div>

      <div class="card" onclick="openService('Jasa Desain Renovasi Rumah','RENDER-CLASIC/service-renovasi.jpg')">
        <div>Jasa Desain Renovasi Rumah</div>
      </div>

    </div>
  </section>

  <!-- SERVICE MODAL -->
  <div id="serviceModal" class="modal" onclick="closeService()">
    <div class="modal-content" onclick="event.stopPropagation()">
      <h3 id="serviceTitle"></h3>
      <img id="serviceImg" src="" style="width:100%;max-height:420px;object-fit:contain;margin:20px 0;">
      <a id="downloadBtn" href="#" download style="display:inline-block;margin-top:10px;border:1px solid #262626;padding:12px 24px;font-size:13px;">Download Poster</a>
      <div class="close-btn" onclick="closeService()">Tutup</div>
    </div>
  </div>

<section id="contact">
  <div class="section-title">Connect With Us</div>

  <div class="social-clean">
    <!-- WhatsApp -->
    <a href="https://wa.me/6281234567890" target="_blank" aria-label="WhatsApp">
      <i class="fab fa-whatsapp"></i>
    </a>

    <!-- Instagram -->
    <a href="https://www.instagram.com/rataatapstudio" target="_blank" aria-label="Instagram">
      <i class="fab fa-instagram"></i>
    </a>

    <!-- TikTok -->
    <a href="https://www.tiktok.com/@rataatapstudio" target="_blank" aria-label="TikTok">
      <i class="fab fa-tiktok"></i>
    </a>

    <!-- YouTube -->
    <a href="https://www.youtube.com/@rataatapstudio" target="_blank" aria-label="YouTube">
      <i class="fab fa-youtube"></i>
    </a>
  </div>
</section>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">

  <!-- FOOTER -->
  <footer>
    © 2025 Rataatap Studio. All rights reserved.
  </footer>

  <script>
    // Smooth scroll offset for fixed navbar
    const links = document.querySelectorAll('a[href^="#"]');
    links.forEach(link => {
      link.addEventListener('click', e => {
        e.preventDefault();
        const target = document.querySelector(link.getAttribute('href'));
        if (!target) return;
        const offset = 80;
        const top = target.offsetTop - offset;
        window.scrollTo({ top, behavior: 'smooth' });
      });
    });
  
    // Toggle Team Section
    const teamBtn = document.getElementById('teamToggle');
    const teamSection = document.getElementById('teamSection');

    teamBtn.addEventListener('click', () => {
      const isOpen = teamSection.style.display === 'block';
      teamSection.style.display = isOpen ? 'none' : 'block';
      teamBtn.textContent = isOpen ? 'Lihat Tim Kami' : 'Tutup Tim';
    });
  
    function openModal(title, desc, img) {
      document.getElementById('modalTitle').innerText = title;
      document.getElementById('modalDesc').innerText = desc;
      document.getElementById('modalImg').src = img;
      document.getElementById('teamModal').style.display = 'flex';
    }

    function closeModal() {
      document.getElementById('teamModal').style.display = 'none';
    }
  
    // SERVICE MODAL
    function openService(title, img) {
      document.getElementById('serviceTitle').innerText = title;
      document.getElementById('serviceImg').src = img;
      document.getElementById('downloadBtn').href = img;
      document.getElementById('serviceModal').style.display = 'flex';
    }

    function closeService() {
      document.getElementById('serviceModal').style.display = 'none';
    }
  </script>

</body>
</html>

