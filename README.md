<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Muay One Boxing</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-image: url('1a4e28a0-2521-46ab-a037-10c59461b0e1.png');
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
      background-attachment: fixed;
    }
    header {
      background-color: rgba(0, 0, 0, 0.8);
      color: white;
      text-align: center;
      padding: 20px 10px;
      position: sticky;
      top: 0;
      z-index: 999;
    }
    nav {
      background-color: #cc0000;
      display: flex;
      justify-content: center;
      gap: 20px;
      padding: 10px;
    }
    nav a {
      color: white;
      text-decoration: none;
      font-weight: bold;
    }
    section {
      padding: 20px;
    }
    .services, .products, .contact-form {
      background: rgba(255, 255, 255, 0.9);
      padding: 20px;
      margin: 20px auto;
      border-radius: 10px;
      max-width: 800px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    h2 {
      color: #cc0000;
    }
    .service, .product {
      margin-bottom: 10px;
    }
    form input, form textarea, form button {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    button {
      background-color: #cc0000;
      color: white;
      font-weight: bold;
      border: none;
      cursor: pointer;
    }
  </style>
</head>
<body>

<header>
  <h1>Muay One Boxing Center</h1>
  <p>Chuyên đào tạo Muay Thái - Boxing - PT cá nhân</p>
</header>

<nav>
  <a href="#services">Gói tập</a>
  <a href="#products">Dụng cụ</a>
  <a href="#contact">Đăng ký</a>
</nav>

<section id="services" class="services">
  <h2>Dịch vụ & Gói tập</h2>
  <div class="service">
    <strong>Phong trào (Premium):</strong> 1 tháng 500K, nửa tháng 350K, 1 ngày 40K
  </div>
  <div class="service">
    <strong>Tự do (Basic):</strong> 1 tháng 300K, nửa tháng 200K, 1 ngày 30K
  </div>
  <div class="service">
    <strong>1:1 cùng HLV (PT):</strong> 1 tháng 3-4 triệu, 1 buổi 450K
  </div>
  <div class="service">
    <strong>Gói gia đình:</strong> 1 tháng 4-5 triệu, 1 buổi 600K
  </div>
  <div class="service">
    <strong>Lớp trẻ em (KID):</strong> Thứ 7-CN, 16:30 – 1 tháng 350K
  </div>
</section>

<section id="products" class="products">
  <h2>Dụng cụ & Phụ kiện Boxing</h2>
  <div class="product">🥋 Quần Muay Thái / Boxing</div>
  <div class="product">🥊 Bao tay Boxing</div>
  <div class="product">🩹 Băng đa Boxing</div>
  <div class="product">🦵 Giáp chân</div>
  <div class="product">👕 Áo Muay One (M.O)</div>
  <div class="product">🧦 Tất tập luyện</div>
  <div class="product">🛡️ Bảo hộ chân</div>
  <div class="product">🧤 Bảo hộ tay</div>
  <div class="product">🧼 Dịch vụ giặt & làm sạch: băng đa, bao tay, giáp chân</div>
</section>

<section id="contact" class="contact-form">
  <h2>Đăng ký tập thử / tư vấn</h2>
  <form onsubmit="return handleSubmit(event)">
    <input type="text" id="name" placeholder="Họ tên" required>
    <input type="tel" id="phone" placeholder="Số điện thoại" required>
    <textarea id="message" placeholder="Nội dung cần tư vấn hoặc gói muốn đăng ký" required></textarea>
    <button type="submit">Gửi đăng ký</button>
  </form>
  <div id="confirmation" style="display:none; color: green; margin-top: 10px;">
    ✅ Đăng ký của bạn đã được gửi! Chúng tôi sẽ liên hệ sớm nhất.
  </div>
</section>

<script>
  const scriptURL = https://script.google.com/macros/s/AKfycby0vqfaGNasPWZfjsKUD_33uRoyg0SOmy--1CeThcTumcgd0uFu6kcFMshAnCydirLiDg/exec;

  function handleSubmit(e) {
    e.preventDefault();
    const name = document.getElementById('name').value;
    const phone = document.getElementById('phone').value;
    const message = document.getElementById('message').value;

    fetch(scriptURL, {
      method: 'POST',
      body: JSON.stringify({ name, phone, message }),
      headers: { 'Content-Type': 'application/json' }
    })
    .then(response => {
      document.getElementById('confirmation').style.display = 'block';
      e.target.reset();
    })
    .catch(error => alert('Đã xảy ra lỗi. Vui lòng thử lại sau.'));
  }
</script>
</body>
</html>
