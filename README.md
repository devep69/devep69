<!DOCTYPE html>
<html lang="vi">
    <style>
    body {
    background: #000;
    color: #00ff00;
    text-align: center;
    font-family: Arial, sans-serif;
    }
    .led-counter {
        font-size: 40px;
        letter-spacing: 5px;
        margin: 20px 0;
    }
    </style>
<head>
    <meta charset="UTF-8">
    <title>View Counter</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h2>Software Developer</h2>
    <div id="counter" class="led-counter">000000</div>
    <script>
        document.addEventListener('DOMContentLoaded', () => {
        let views = localStorage.getItem('pageViews') || 0;
        views = parseInt(views) + 1;
        localStorage.setItem('pageViews', views);
        // Hiển thị số với 6 chữ số, thêm số 0 phía trước
        const counter = document.getElementById('counter');
        counter.textContent = String(views).padStart(6, '0');
        });
    </script>
</body>
</html>