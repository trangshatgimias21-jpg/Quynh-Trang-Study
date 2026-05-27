<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Quynh Trang Study</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600;700&family=Be+Vietnam+Pro:wght@300;400;500;600;700&display=swap" rel="stylesheet">

  <style>
    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
    }

    :root{
      --navy:#081f5c;
      --light:#f7f8fc;
      --beige:#efe3cf;
      --text:#1f2937;
      --white:#ffffff;
      --shadow:0 8px 25px rgba(0,0,0,0.08);
    }

    html{
      scroll-behavior:smooth;
    }

    body{
      font-family:'Be Vietnam Pro',sans-serif;
      background:var(--light);
      color:var(--text);
      line-height:1.6;
    }

    a{
      text-decoration:none;
    }

    .container{
      width:min(1200px,92%);
      margin:auto;
    }

    header{
      background:var(--white);
      position:sticky;
      top:0;
      z-index:1000;
      box-shadow:0 2px 10px rgba(0,0,0,0.05);
    }

    .navbar{
      display:flex;
      justify-content:space-between;
      align-items:center;
      padding:18px 0;
    }

    .logo{
      display:flex;
      flex-direction:column;
      color:var(--navy);
    }

    .logo h1{
      font-family:'Playfair Display',serif;
      font-size:34px;
      line-height:1;
    }

    .logo span{
      letter-spacing:4px;
      font-size:13px;
      margin-top:6px;
      font-weight:600;
    }

    nav{
      display:flex;
      gap:30px;
      align-items:center;
    }

    nav a{
      color:var(--navy);
      font-weight:600;
      transition:0.3s;
    }

    nav a:hover{
      color:#c59d5f;
    }

    .phone-btn{
      background:var(--navy);
      color:white;
      padding:12px 22px;
      border-radius:999px;
      font-weight:600;
    }

    .hero{
      padding:90px 0 70px;
      background:linear-gradient(to right,#ffffff,#eef2ff);
    }

    .hero-grid{
      display:grid;
      grid-template-columns:1.1fr 0.9fr;
      gap:40px;
      align-items:center;
    }

    .hero h2{
      font-size:70px;
      line-height:1.05;
      color:var(--navy);
      font-family:'Playfair Display',serif;
    }

    .hero .sub{
      margin:20px 0;
      font-size:26px;
      color:#7c5d2f;
      font-weight:600;
    }

    .hero p{
      max-width:650px;
      font-size:17px;
      color:#4b5563;
    }

    .hero-buttons{
      display:flex;
      gap:18px;
      margin-top:35px;
      flex-wrap:wrap;
    }

    .btn{
      padding:15px 28px;
      border-radius:14px;
      font-weight:600;
      transition:0.3s;
      display:inline-flex;
      align-items:center;
      gap:10px;
    }

    .btn-primary{
      background:var(--navy);
      color:white;
    }

    .btn-primary:hover{
      transform:translateY(-2px);
    }

    .btn-outline{
      border:2px solid var(--navy);
      color:var(--navy);
      background:white;
    }

    .hero-card{
      background:white;
      border-radius:28px;
      padding:40px;
      box-shadow:var(--shadow);
    }

    .hero-card h3{
      color:var(--navy);
      font-size:30px;
      margin-bottom:20px;
    }

    .hero-card ul{
      list-style:none;
    }

    .hero-card li{
      padding:14px 0;
      border-bottom:1px solid #ececec;
      font-weight:500;
    }

    .hero-card li:last-child{
      border:none;
    }

    section{
      padding:80px 0;
    }

    .section-title{
      text-align:center;
      margin-bottom:50px;
    }

    .section-title h3{
      font-size:42px;
      color:var(--navy);
      font-family:'Playfair Display',serif;
      margin-bottom:12px;
    }

    .section-title p{
      color:#6b7280;
    }

    .feature-grid{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(240px,1fr));
      gap:25px;
    }

    .feature-card{
      background:white;
      padding:30px;
      border-radius:22px;
      box-shadow:var(--shadow);
      transition:0.3s;
    }

    .feature-card:hover{
      transform:translateY(-5px);
    }

    .feature-card .icon{
      width:65px;
      height:65px;
      border-radius:18px;
      background:#edf2ff;
      display:flex;
      align-items:center;
      justify-content:center;
      font-size:28px;
      margin-bottom:20px;
    }

    .feature-card h4{
      color:var(--navy);
      margin-bottom:10px;
      font-size:22px;
    }

    .class-section{
      background:white;
    }

    .class-grid{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(260px,1fr));
      gap:25px;
    }

    .class-card{
      background:var(--light);
      border-radius:22px;
      padding:30px;
      border:1px solid #edf0f5;
      transition:0.3s;
    }

    .class-card:hover{
      border-color:#c7d2fe;
      transform:translateY(-5px);
    }

    .class-card h4{
      color:var(--navy);
      margin-bottom:14px;
      font-size:24px;
    }

    .class-card ul{
      padding-left:18px;
      color:#4b5563;
    }

    .homework-grid{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
      gap:25px;
    }

    .homework-card{
      background:white;
      border-radius:22px;
      padding:30px;
      box-shadow:var(--shadow);
    }

    .homework-card h4{
      color:var(--navy);
      font-size:24px;
      margin-bottom:15px;
    }

    .homework-card p{
      margin-bottom:25px;
      color:#6b7280;
    }

    .mini-btn{
      background:var(--navy);
      color:white;
      padding:12px 20px;
      border-radius:12px;
      display:inline-block;
      font-weight:600;
    }

    .notice-wrapper{
      display:grid;
      grid-template-columns:1fr 1fr;
      gap:30px;
    }

    .notice-box{
      background:white;
      border-radius:24px;
      padding:35px;
      box-shadow:var(--shadow);
    }

    .notice-box h4{
      font-size:28px;
      color:var(--navy);
      margin-bottom:20px;
    }

    .notice-item{
      padding:18px 0;
      border-bottom:1px solid #ececec;
    }

    .notice-item:last-child{
      border:none;
    }

    .contact-section{
      background:linear-gradient(135deg,var(--navy),#12318b);
      color:white;
      border-radius:30px;
      padding:60px;
    }

    .contact-grid{
      display:grid;
      grid-template-columns:1fr 1fr;
      gap:40px;
      align-items:center;
    }

    .contact-section h3{
      font-size:48px;
      margin-bottom:20px;
      font-family:'Playfair Display',serif;
    }

    .contact-info p{
      margin-bottom:14px;
      font-size:18px;
    }

    .contact-form{
      background:white;
      padding:30px;
      border-radius:24px;
    }

    .contact-form input,
    .contact-form textarea{
      width:100%;
      padding:15px;
      border:1px solid #dcdcdc;
      border-radius:12px;
      margin-bottom:16px;
      font-family:inherit;
    }

    .contact-form button{
      width:100%;
      padding:16px;
      border:none;
      border-radius:12px;
      background:var(--navy);
      color:white;
      font-weight:600;
      cursor:pointer;
    }

    footer{
      background:#06153f;
      color:white;
      text-align:center;
      padding:28px;
      margin-top:80px;
    }

    @media(max-width:980px){
      .hero-grid,
      .notice-wrapper,
      .contact-grid{
        grid-template-columns:1fr;
      }

      nav{
        display:none;
      }

      .hero h2{
        font-size:52px;
      }

      .contact-section{
        padding:40px 25px;
      }
    }

    @media(max-width:640px){
      .hero{
        padding:70px 0 50px;
      }

      .hero h2{
        font-size:42px;
      }

      .section-title h3{
        font-size:34px;
      }

      .navbar{
        flex-direction:column;
        gap:18px;
      }

      .hero-buttons{
        flex-direction:column;
      }

      .btn{
        justify-content:center;
      }
    }
  </style>
</head>
<body>

<header>
  <div class="container navbar">
    <div class="logo">
      <h1>Quynh Trang</h1>
      <span>STUDY</span>
    </div>

    <nav>
      <a href="#home">Trang chủ</a>
      <a href="#about">Giới thiệu</a>
      <a href="#classes">Lớp học</a>
      <a href="#homework">Làm bài</a>
      <a href="#notice">Thông báo</a>
      <a href="#contact">Liên hệ</a>
    </nav>

    <a class="phone-btn" href="tel:0365877361">0365.877.361</a>
  </div>
</header>

<section class="hero" id="home">
  <div class="container hero-grid">

    <div>
      <h2>Quynh Trang Study</h2>
      <div class="sub">Toán – Tư duy – Hiệu quả</div>

      <p>
        Trung tâm chuyên Toán dành cho học sinh THCS – THPT.
        Đồng hành cùng học sinh xây dựng tư duy logic,
        nâng cao kiến thức và tự tin chinh phục mục tiêu.
      </p>

      <div class="hero-buttons">
        <a href="#homework" class="btn btn-primary">📘 Làm bài tập</a>
        <a href="#classes" class="btn btn-outline">🎓 Vào lớp học</a>
      </div>
    </div>

    <div class="hero-card">
      <h3>Điểm nổi bật</h3>

      <ul>
        <li>✔ Dạy dễ hiểu – sát năng lực học sinh</li>
        <li>✔ Bám sát chương trình THCS – THPT</li>
        <li>✔ Theo dõi tiến bộ từng buổi học</li>
        <li>✔ Bài tập và tài liệu cập nhật liên tục</li>
        <li>✔ Đồng hành tận tâm cùng học sinh</li>
      </ul>
    </div>

  </div>
</section>

<section id="about">
  <div class="container">

    <div class="section-title">
      <h3>Vì sao học sinh lựa chọn?</h3>
      <p>Môi trường học tập hiện đại – hiệu quả – tận tâm</p>
    </div>

    <div class="feature-grid">

      <div class="feature-card">
        <div class="icon">📖</div>
        <h4>Dạy dễ hiểu</h4>
        <p>Phương pháp logic, giúp học sinh hiểu bản chất và áp dụng nhanh.</p>
      </div>

      <div class="feature-card">
        <div class="icon">📈</div>
        <h4>Theo dõi tiến bộ</h4>
        <p>Đánh giá định kỳ để học sinh cải thiện điểm số rõ rệt.</p>
      </div>

      <div class="feature-card">
        <div class="icon">📝</div>
        <h4>Bài tập đa dạng</h4>
        <p>Kho bài tập phong phú từ cơ bản đến nâng cao.</p>
      </div>

      <div class="feature-card">
        <div class="icon">💙</div>
        <h4>Đồng hành tận tâm</h4>
        <p>Luôn hỗ trợ học sinh trong quá trình học tập và ôn thi.</p>
      </div>

    </div>
  </div>
</section>

<section class="class-section" id="classes">
  <div class="container">

    <div class="section-title">
      <h3>Các lớp học</h3>
      <p>Lộ trình học phù hợp cho từng cấp học</p>
    </div>

    <div class="class-grid">

      <div class="class-card">
        <h4>Toán 6 – 7 – 8 – 9</h4>
        <ul>
          <li>Củng cố kiến thức nền</li>
          <li>Rèn kỹ năng giải toán</li>
          <li>Phát triển tư duy logic</li>
        </ul>
      </div>

      <div class="class-card">
        <h4>Toán 10 – 11 – 12</h4>
        <ul>
          <li>Ôn tập theo chuyên đề</li>
          <li>Luyện đề nâng cao</li>
          <li>Bứt phá điểm số</li>
        </ul>
      </div>

      <div class="class-card">
        <h4>Luyện thi vào 10</h4>
        <ul>
          <li>Bám sát cấu trúc đề thi</li>
          <li>Hệ thống kiến thức trọng tâm</li>
          <li>Rèn tốc độ làm bài</li>
        </ul>
      </div>

      <div class="class-card">
        <h4>Luyện thi THPTQG</h4>
        <ul>
          <li>Chiến lược đạt điểm cao</li>
          <li>Tổng hợp dạng bài thường gặp</li>
          <li>Ôn tập chuyên sâu</li>
        </ul>
      </div>

    </div>
  </div>
</section>

<section id="homework">
  <div class="container">

    <div class="section-title">
      <h3>Làm bài tập online</h3>
      <p>Chỉ cần thay link Google Forms vào nút bên dưới</p>
    </div>

    <div class="homework-grid">

      <div class="homework-card">
        <h4>Bài tập lớp 9</h4>
        <p>Trắc nghiệm chương Hàm số và Hình học.</p>
        <a href="https://forms.google.com" target="_blank" class="mini-btn">Làm bài</a>
      </div>

      <div class="homework-card">
        <h4>Kiểm tra lớp 10</h4>
        <p>Ôn tập Đại số – Hình học theo chuyên đề.</p>
        <a href="https://forms.google.com" target="_blank" class="mini-btn">Làm bài</a>
      </div>

      <div class="homework-card">
        <h4>Luyện thi THPTQG</h4>
        <p>Đề tổng hợp mức độ nhận biết đến vận dụng cao.</p>
        <a href="https://forms.google.com" target="_blank" class="mini-btn">Làm bài</a>
      </div>

    </div>
  </div>
</section>

<section id="notice">
  <div class="container notice-wrapper">

    <div class="notice-box">
      <h4>Thông báo mới</h4>

      <div class="notice-item">
        📌 Khai giảng lớp hè tháng 6
      </div>

      <div class="notice-item">
        📌 Cập nhật lịch học mới
      </div>

      <div class="notice-item">
        📌 Đã đăng tải tài liệu ôn tập
      </div>

      <div class="notice-item">
        📌 Nhận đăng ký lớp luyện thi vào 10
      </div>
    </div>

    <div class="notice-box">
      <h4>Thông tin trung tâm</h4>

      <div class="notice-item">
        ☎ Hotline: 0365.877.361
      </div>

      <div class="notice-item">
        🎓 Chuyên môn: Toán THCS – THPT
      </div>

      <div class="notice-item">
        📚 Học online & offline
      </div>

      <div class="notice-item">
        💙 Đồng hành cùng học sinh mỗi ngày
      </div>
    </div>

  </div>
</section>

<section id="contact">
  <div class="container contact-section">

    <div class="contact-grid">

      <div class="contact-info">
        <h3>Liên hệ tư vấn</h3>

        <p>📞 0365.877.361</p>
        <p>📘 Quynh Trang Study</p>
        <p>🎓 Chuyên Toán THCS – THPT</p>
        <p>💬 Hỗ trợ học sinh và phụ huynh nhanh chóng</p>
      </div>

      <div class="contact-form">
        <input type="text" placeholder="Họ và tên">
        <input type="tel" placeholder="Số điện thoại">
        <textarea rows="5" placeholder="Nội dung cần tư vấn"></textarea>
        <button>Gửi thông tin</button>
      </div>

    </div>

  </div>
</section>

<footer>
  Quynh Trang Study © 2026 — Đồng hành cùng học sinh chinh phục môn Toán.
</footer>

</body>
</html>
