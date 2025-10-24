<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Website Bảo Mật</title>
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body {
      font-family: 'Arial', sans-serif;
      background: linear-gradient(to bottom, #89f7fe, #66a6ff);
      color: #333;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: flex-start;
      padding: 20px;
    }

    h1, h2 { margin-bottom: 15px; }

    #content {
      display: none; /* ẩn ban đầu */
      background: #fff;
      border-radius: 15px;
      padding: 20px;
      width: 100%;
      max-width: 500px;
      box-shadow: 0 8px 20px rgba(0,0,0,0.2);
      text-align: center;
      margin-top: 30px;
      animation: fadeIn 0.5s ease-in-out;
    }

    video {
      width: 100%;
      height: auto;
      border-radius: 10px;
      margin-top: 15px;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    p { margin-top: 10px; }
  </style>
  <script>
    function askPassword() {
      const password = prompt("Nhập mật khẩu để truy cập website:");
      if(password === "123456") { // Thay mật khẩu bạn muốn
        document.getElementById("content").style.display = "block";
      } else {
        alert("Sai mật khẩu! Không thể truy cập.");
        window.location.reload();
      }
    }
    window.onload = askPassword;
  </script>
</head>
<body>
  <h1>Chào mừng đến Website của tôi!</h1>

  <div id="content">
    <h2>Nội dung bảo vệ mật khẩu</h2>
    <p>Chỉ người có mật khẩu mới xem được nội dung này.</p>

    <!-- Video trực tiếp của bạn -->
    <video controls>
      <source src="https://video.twimg.com/amplify_video/1948027641371717632/vid/avc1/320x584/K8UcMSYcscIRBG2J.mp4?tag=14" type="video/mp4">
      Trình duyệt của bạn không hỗ trợ video.
    </video>
  </div>
</body>
</html>
