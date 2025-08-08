<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Yusuf Ath Thaariq | Mahasiswa Statistika</title>

  <!-- AOS Animation CSS -->
  <link href="https://cdn.jsdelivr.net/npm/aos@2.3.4/dist/aos.css" rel="stylesheet">
  <!-- Typed.js -->
  <script src="https://cdn.jsdelivr.net/npm/typed.js@2.0.12"></script>

  <style>
    :root {
      --primary-color: #4b0082;
      --secondary-color: #6a0dad;
      --background-light: #ffffff;
      --background-dark: #1e1e1e;
      --text-light: #333333;
      --text-dark: #f1f1f1;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      margin: 0;
      padding: 0;
      background-color: var(--background-light);
      color: var(--text-light);
      transition: background-color 0.3s, color 0.3s;
    }

    .dark-mode {
      background-color: var(--background-dark);
      color: var(--text-dark);
    }

    header {
      background-image: url('Cat 10.jpeg');
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
      color: white;
      text-align: center;
      padding: 40px 20px;
      position: relative;
}

header h1:hover {
  animation: wiggle 0.3s ease-in-out infinite;
  cursor: pointer;
}

@keyframes wiggle {
  0%, 100% { transform: rotate(0deg); }
  25% { transform: rotate(3deg); }
  75% { transform: rotate(-3deg); }
}

li:hover {
  transform: scale(1.05);
  transition: transform 0.2s ease-in-out;
  color: #6a0dad;
}

    header img {
      width: 120px;
      height: 120px;
      border-radius: 50%;
      border: 4px solid white;
      margin-bottom: 15px;
    }

    nav {
      background-color: var(--secondary-color);
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      padding: 12px;
    }

    nav a {
      color: white;
      text-decoration: none;
      margin: 10px 15px;
      font-weight: bold;
      font-size: 16px;
    }

    nav a:hover {
      text-decoration: underline;
    }

    .container {
      max-width: 1000px;
      margin: 40px auto;
      padding: 20px;
      background-color: white;
      border-radius: 15px;
      box-shadow: 0 4px 20px rgba(0,0,0,0.1);
    }

    .dark-mode .container {
      background-color: #2c2c2c;
    }

    h2 {
      color: var(--primary-color);
      margin-bottom: 15px;
    }

    section p, section ul {
      font-size: 18px;
      line-height: 1.7;
      text-align: justify;
    }

    li:hover {
      transform: scale(1.02);
      transition: all 0.3s ease;
      background-color: #f0f0f0;
      border-radius: 10px;
      padding: 5px;
    }

    footer {
      background-color: var(--primary-color);
      color: white;
      text-align: center;
      padding: 20px;
      margin-top: 50px;
    }

    .toggle-mode {
      position: fixed;
      top: 20px;
      right: 20px;
      background: #fff;
      border: none;
      padding: 10px 15px;
      border-radius: 10px;
      cursor: pointer;
      font-weight: bold;
      box-shadow: 0 2px 10px rgba(0,0,0,0.2);
    }

    .dark-mode .toggle-mode {
      background-color: #444;
      color: white;
    }
li span {
      color: var(--primary-color);
      cursor: pointer;
      display: inline-flex;
      align-items: center;
      gap: 8px;
      transition: color 0.2s;
    }

    li span:hover {
      color: #8a2be2;
    }

    .description {
      max-height: 0;
      overflow: hidden;
      opacity: 0;
      transition: max-height 0.5s ease, opacity 0.5s ease;
      font-size: 16px;
      margin-top: 5px;
      color: #555;
    }

    .description.show {
      max-height: 200px;
      opacity: 1;
    }

  /* Zoom Modal */
    .modal {
      display: none;
      position: fixed;
      z-index: 999;
      padding-top: 60px;
      left: 0;
      top: 0;
      width: 50%;
      height: 50%;
      overflow: auto;
      background-color: rgba(0,0,0,0.8);
    }

    .modal-content {
      margin: auto;
      display: block;
      max-width: 80%;
    }

    .modal-content, .modal {
      animation-name: zoom;
      animation-duration: 0.3s;
    }

    @keyframes zoom {
      from {transform: scale(0)}
      to {transform: scale(1)}
    }

    .close {
      position: absolute;
      top: 20px;
      right: 35px;
      color: #fff;
      font-size: 40px;
      font-weight: bold;
      cursor: pointer;
    }

    @media (max-width: 600px) {
      header h1 {
        font-size: 26px;
      }
    }

    #topBtn {
      display: none;
      position: fixed;
      bottom: 40px;
      right: 30px;
      z-index: 99;
      border: none;
      background-color: var(--primary-color);
      color: white;
      cursor: pointer;
      padding: 10px 15px;
      border-radius: 10px;
    }

    #topBtn:hover {
      background-color: #333;
    }
  </style>
</head>
<body>
  <button class="toggle-mode" onclick="toggleDarkMode()">🌙 Mode Gelap</button>
  <button onclick="scrollToTop()" id="topBtn" title="Kembali ke atas">⬆</button>

  <header>
    <img src= "file:///C:/Users/User/Desktop/HTML/Profile Website.jpg" alt="Foto Saya">
    <h1>Yusuf Ath Thaariq Al Fath</h1>
    <p>Mahasiswa Statistika | Universitas Diponegoro</p>
    <p><span class="typed-text"></span></p>
  </header>

  <div id="imgModal" class="modal">
    <span class="close" onclick="closeModal()">&times;</span>
    <img class="modal-content" id="modalImage">
  </div>

  <nav>
    <a href="#tentang">Tentang</a>
    <a href="#pendidikan">Pendidikan</a>
    <a href="#proyek">Proyek</a>
    <a href="#organisasi">Organisasi</a>
    <a href="#panitia">Kepanitiaan</a>
    <a href="#sertifikat">Sertifikat</a>
    <a href="#sertifikat">Keahlian</a>
    <a href="#kontak">Kontak</a>
  </nav>

  <section id="tentang" class="container"  data-aos="fade-up">
    <h2>Tentang Saya</h2>
    <p>
      Halo! Saya <strong>Yusuf Ath Thaariq Al Fath</strong>, mahasiswa Statistika Universitas Diponegoro angkatan 2024. Saya tertarik pada analisis data, teknologi statistik, dan pengembangan sistem informasi. Saya juga aktif dalam organisasi dan suka mengeksplorasi hal-hal baru yang berhubungan dengan data dan visualisasi.
    </p>
  </section>

  <section id="pendidikan" class="container" data-aos="fade-right">
    <h2>Riwayat Pendidikan</h2>
    <ul>
      <li>KB TK Hj Isriati Baiturrahman 2</li>
      <li>SD Hj Isriati Baiturrahman 2</li>
      <li>SMP Hj Isriati</li>
      <li>SMA Negeri 06 Semarang</li>
      <li>Statistika, Universitas Diponegoro (2024 - sekarang)</li>
    </ul>
  </section>

  <section id="proyek" class="container" data-aos="zoom-in">
    <h2>Proyek Statistik</h2>
    <ul>
      <li>Analisis Korelasi antara Dividen dan Harga Saham menggunakan SPSS</li>
      <li>Model Prediksi Banjir Rob berbasis LSTM dan GUI R (Proposal PKM-RE)</li>
      <li>Dashboard Interaktif Pengiriman Paket dengan R Shiny</li>
    </ul>
  </section>

<section id="organisasi" class="container" data-aos="fade-left">
    <h2>Organisasi</h2>
    <ul>
      <li>
        <span onclick="toggleDescription(this)">Organisasi Intra Sekolah SMP Hj. Isriati <span class="arrow">🔽</span></span>
        <div class="description">
          <h3>Wakil Ketua</h3>
          <p>Menjabat sebagai Wakil Ketua OSIS di SMP H Isriati. Memainkan peran penting dalam mendukung Ketua OSIS dalam mengoordinasikan berbagai kegiatan sekolah dan memastikan pelaksanaan program organisasi berjalan lancar. Memimpin rapat dan mengambil keputusan penting saat Ketua OSIS tidak hadir, berkolaborasi dengan anggota OSIS lainnya untuk menciptakan lingkungan sekolah yang aktif dan positif.</p>
        </div>
      </li>

      <li>
        <span onclick="toggleDescription(this)">Rohani Islam SMA Negeri 06 Semarang<span class="arrow">🔽</span></span>
        <div class="description">
          <h3>Divisi IT</h3>
          <p>Bertugas sebagai anggota Divisi Teknologi Informasi (IT) di ROHIS SMAN 6 Semarang selama dua periode pada tahun ajaran 2022/2023 dan 2023/2024. Bertanggung jawab atas pengelolaan platform digital untuk komunikasi dan promosi kegiatan keagamaan. Bekerja sama dengan tim untuk memastikan operasional teknologi berjalan lancar selama acara, serta membantu dalam pembuatan konten multimedia untuk mendukung kegiatan dan upaya penyuluhan.</p>
        </div>
      </li>

      <li>
        <span onclick="toggleDescription(this)">Rohani Islam SMA Kota Semarang<span class="arrow">🔽</span></span>
        <div class="description">
          <h3>Dewan Evaluasi</h3>
          <p>Bertugas sebagai anggota Dewan Evaluasi di ROHIS SMA Kota Semarang selama satu periode pada tahun ajaran 2023/2024. Bertanggung jawab untuk menilai dan mengevaluasi kinerja serta pelaksanaan program-program keagamaan. Bekerja sama dengan anggota lain untuk memberikan masukan konstruktif dan rekomendasi untuk peningkatan, dengan tujuan meningkatkan efektivitas kegiatan dan perkembangan spiritual anggota.</p>
        </div>
      </li>

      <li>
        <span onclick="toggleDescription(this)">Naungan Ukhuwah Iman dan Islam Statistika<span class="arrow">🔽</span></span>
        <div class="description">
          <h3>Kaderisasi</h3>
          <p>Bertugas sebagai anggota staf di Divisi kaderisasi NUANSA (Naungan Ukhuwah Iman dan Islam Statistika). Bertanggung jawab dalam mendukung perencanaan dan pelaksanaan program regenerasi, termasuk rekrutmen anggota, pelatihan, dan kegiatan pengembangan internal. Berkolaborasi dengan anggota divisi untuk memperkuat nilai-nilai Islam dan kesinambungan organisasi di antara anggota.</p>
        </div>
      </li>
    </ul>
  </section>

<section id="panitia" class="container" data-aos="fade-up">
    <h2>Kepanitiaan</h2>
    <ul>
      <li>
        <span onclick="toggleDescription(this)">Generasi Mahir Berteknologi (GEMARI) <span class="arrow">🔽</span></span>
        <div class="description">Menjadi panitia dalam kegiatan Gerakan Mahir Berteknologi (GEMARI) sebagai anggota divisi Perlengkapan dan Fasilitator. Bertanggung jawab dalam menyiapkan dan mengelola kebutuhan perlengkapan kegiatan, memastikan kelancaran aspek teknis, serta mendampingi peserta selama sesi pelatihan dengan memberikan panduan dan materi. Bekerja sama dengan tim untuk memastikan kegiatan berjalan lancar dan efektif</div>
      </li>
      <li>
        <span onclick="toggleDescription(this)" >SMAN 06 Semarang Festival (Smansix Fest) <span class="arrow">🔽</span></span>
        <div class="description">Menjadi panitia dalam kegiatan SMANSIX Fest sebagai anggota divisi Perlengkapan dan Penjaga Stand Booth Kampus. Bertanggung jawab dalam menyiapkan dan mengatur kebutuhan logistik acara serta menjaga booth kampus untuk memberikan informasi kepada pengunjung secara aktif. Berkontribusi dalam menciptakan suasana acara yang tertib dan informatif.</div>
      </li>
      <li>
        <span onclick="toggleDescription(this)" >Serah Terima Jabatan Himpunan Mahasiswa Statistika 2025 <span class="arrow">🔽</span></span>
        <div class="description">Menjadi panitia dalam kegiatan Serah Terima Jabatan Himpunan Statistika 2025 sebagai anggota divisi Acara. Bertanggung jawab dalam menyusun rangkaian acara, mengatur jalannya kegiatan, serta memastikan setiap sesi berlangsung sesuai dengan rundown. Bekerja sama dengan tim untuk menciptakan acara yang tertib, khidmat, dan berkesan.</div>
      </li>
      <li>
        <span onclick="toggleDescription(this)" >Dokter Data <span class="arrow">🔽</span></span>
        <div class="description" >Menjadi panitia dalam kegiatan Dokter Data sebagai anggota divisi Acara. Bertanggung jawab dalam merancang alur kegiatan, menyusun susunan acara, serta memastikan setiap sesi berjalan lancar sesuai jadwal. Bekerja sama dengan tim untuk menciptakan pengalaman acara yang edukatif, interaktif, dan tertata dengan baik.</div>
      </li>
      <li>
        <span onclick="toggleDescription(this)" >Latihan Keterampilan Manajemen Mahasiswa Pra-Dasar <span class="arrow">🔽</span></span>
        <div class="description" >Menjadi panitia dalam kegiatan LKMMPD sebagai anggota divisi Fasilitator. Bertugas mendampingi peserta selama kegiatan, menyampaikan materi, serta membimbing diskusi dan aktivitas kelompok. Berperan aktif dalam menciptakan suasana pembelajaran yang kondusif dan mendukung pengembangan soft skills peserta.</div>
      </li>
      <li>
        <span onclick="toggleDescription(this)" >Training Rohis I <span class="arrow">🔽</span></span>
        <div class="description" >Menjadi Ketua Pelaksana dalam kegiatan Training Rohis 1. Bertanggung jawab penuh dalam merancang konsep acara, mengoordinasikan seluruh divisi panitia, serta memastikan kegiatan berjalan sesuai dengan tujuan dan jadwal yang telah direncanakan. Memimpin evaluasi tim dan mengambil keputusan strategis untuk kelancaran dan keberhasilan acara.</div>
      </li>
    </ul>
  </section>

  <section id="sertifikat" class="container" data-aos="zoom-in">
    <h2>Sertifikat & Pelatihan</h2>
    <ul>
      <li>
        <span onclick="toggleDescription(this)"> Training Software Statistik <span class="arrow">🔽</span></span>
        <div class="description">Pelatihan dasar yang membahas pengenalan Python, R, dan dasar analisis data.</div>
      </li>
      <li>
        <span onclick="toggleDescription(this)">Seminar Nasional Statistika dan Big Data 2025 <span class="arrow">🔽</span></span>
        <div class="description"> Seminar nasional yang menghadirkan pembicara dari akademisi yang membahas isu dan tren besar dalam big data.</div>
      </li>
    </ul>
  </section>

  <section id="keahlian" class="container" data-aos="fade-up">
  <h2>Keahlian</h2>
  <ul>
    <li>Research</li>
    <li>Public Speaking</li>
    <li>Leadership</li>
    <li>Problem solving</li>
    <li>Basic data analysis</li>
    <li>Basic python programming</li>
    <li>Basic R programming</li>
    <li>Basic SQL programming</li>
    <li>50% ability in English and 100% Indonesia language</li>
  </ul>
</section>


  <section id="kontak" class="container" data-aos="fade-down">
    <h2>Kontak</h2>
    <ul>
      <li>Email: yusufatthaariqalfath@gmail.com</li>
      <li>Instagram: <a href="https://instagram.com/yusuf_atthaariq" target="_blank">@yusuf_atthaariq</a></li>
      <li>LinkedIn: <a href="https://linkedin.com/in/YusufAthThaariqAlFath" target="_blank">linkedin.com/in/Yusuf Ath Thaariq Al Fath</a></li>
    </ul>
  </section>

  <footer>
    &copy; 2025 Yusuf Ath Thaariq Al Fath. Dibuat dengan semangat belajar dan eksplorasi.
  </footer>

  <!-- JS -->
  <script>
    function toggleDarkMode() {
      document.body.classList.toggle("dark-mode");
    }
    function scrollToTop() {
      window.scrollTo({ top: 0, behavior: "smooth" });
    }
    window.onscroll = function () {
      const btn = document.getElementById("topBtn");
      btn.style.display = (document.documentElement.scrollTop > 300) ? "block" : "none";
    };
    var typed = new Typed(".typed-text", {
      strings: ["Mahasiswa Statistika", "Data Enthusiast", "Calon Data Scientist 🔍"],
      typeSpeed: 50,
      backSpeed: 25,
      loop: true
    });
   function toggleDescription(element) {
      const desc = element.nextElementSibling;
      const arrow = element.querySelector(".arrow");
      desc.classList.toggle("show");

      if (desc.classList.contains("show")) {
        arrow.textContent = "🔼";
      } else {
        arrow.textContent = "🔽";
      }
    }
  // Zoom image script //
    const profileImg = document.getElementById("profileImg");
    const modal = document.getElementById("imgModal");
    const modalImage = document.getElementById("modalImage");

    profileImg.onclick = function() {
      modal.style.display = "block";
      modalImage.src = this.src;
    }

    function closeModal() {
      modal.style.display = "none";
    }

    window.onclick = function(event) {
      if (event.target === modal) {
        closeModal();
      }
    }
  </script>
  <script src="https://cdn.jsdelivr.net/npm/aos@2.3.4/dist/aos.js"></script>
  <script>AOS.init();</script>

</body>
</html>
