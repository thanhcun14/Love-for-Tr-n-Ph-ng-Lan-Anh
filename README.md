<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Love for Lan Anh</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f7e6ff;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            text-align: center;
        }

        .container {
            background-color: white;
            padding: 20px;
            border-radius: 12px;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.2);
            position: relative;
        }

        .title {
            font-size: 2.5em;
            color: #ff4081;
        }

        .heart-img, .flower-img {
            width: 50px;
            height: 50px;
            position: absolute;
        }

        .heart-img {
            top: -30px;
            left: -30px;
        }

        .flower-img {
            top: -30px;
            right: -30px;
        }

        .button {
            margin-top: 20px;
            padding: 10px 20px;
            background-color: #ff4081;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .message {
            margin-top: 20px;
            font-size: 1.2em;
            color: #ff4081;
            display: none;
        }

        .counter {
            margin-top: 20px;
            font-size: 1.2em;
        }

        .wolf {
            font-size: 3em;
            margin-top: 20px;
        }

        .first-meet {
            margin-top: 10px;
            font-size: 1.2em;
            color: #888;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1 class="title">Anh yêu em, Lan Anh!</h1>

        <!-- Thêm trái tim và bông hoa -->
        <img class="heart-img" src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/02/Heart_full_red.svg/1024px-Heart_full_red.svg.png" alt="Heart">
        <img class="flower-img" src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/45/Red_rose_icon.svg/1024px-Red_rose_icon.svg.png" alt="Flower">
        
        <p class="counter">Đã yêu nhau được: <span id="daysCounter"></span> ngày</p>
        <!-- Thêm dòng hiển thị ngày lần đầu gặp nhau -->
        <p class="first-meet">Ngày đầu tiên gặp nhau: <span id="firstMeetDate"></span></p>
        
        <button class="button" onclick="showLoveMessage()">Nhấn để biết anh yêu em!</button>
        
        <div class="message" id="loveMessage">
            Trái tim anh mãi thuộc về em! <span class="wolf">🐺</span>
        </div>
    </div>

    <script>
        // Tính số ngày yêu nhau
        function calculateDaysSince(startDate) {
            const today = new Date();
            const diffTime = today - startDate;
            const diffDays = Math.floor(diffTime / (1000 * 60 * 60 * 24));
            return diffDays;
        }

        // Hiển thị thông điệp yêu thương
        function showLoveMessage() {
            document.getElementById('loveMessage').style.display = 'block';
        }

        // Ngày bắt đầu yêu nhau (11/07/2023)
        const startDate = new Date("2023-07-11");
        document.getElementById('daysCounter').textContent = calculateDaysSince(startDate);

        // Ngày lần đầu gặp nhau
        const firstMeetDate = new Date("2023-07-11"); // Ngày đầu tiên gặp nhau
        document.getElementById('firstMeetDate').textContent = firstMeetDate.toLocaleDateString();
    </script>

</body>

</html>
