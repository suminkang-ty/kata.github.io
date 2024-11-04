<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>카탈로그 플립북</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            background-color: #f7f7f7;
        }

        .flipbook {
            position: relative;
            width: 80%;
            max-width: 800px;
            overflow: hidden;
            border: 1px solid #ddd;
        }

        .flipbook img {
            width: 100%;
            display: none;
            transition: transform 0.6s ease;
        }

        .flipbook img.active {
            display: block;
        }

        .flipbook .navigation {
            position: absolute;
            top: 50%;
            width: 100%;
            display: flex;
            justify-content: space-between;
            transform: translateY(-50%);
        }

        .flipbook .nav-button {
            background-color: rgba(0, 0, 0, 0.5);
            color: white;
            padding: 10px;
            cursor: pointer;
            user-select: none;
        }
    </style>
</head>
<body>
    <div class="flipbook">
        <img src="https://www.chilman.co.kr/data/editor/2411/52372d52063ee7aece26b382e036c44e_1730702972_9752.jpg" alt="page1" class="active">
        <img src="https://www.chilman.co.kr/data/editor/2411/52372d52063ee7aece26b382e036c44e_1730702973_1083.jpg" alt="page2">
        <img src="https://www.chilman.co.kr/data/editor/2411/52372d52063ee7aece26b382e036c44e_1730702973_2011.jpg" alt="page3">
        <img src="https://www.chilman.co.kr/data/editor/2411/52372d52063ee7aece26b382e036c44e_1730702973_3591.jpg" alt="page4">
        <img src="https://www.chilman.co.kr/data/editor/2411/52372d52063ee7aece26b382e036c44e_1730702973_4784.jpg" alt="page5">
        <img src="https://www.chilman.co.kr/data/editor/2411/52372d52063ee7aece26b382e036c44e_1730702973_5958.jpg" alt="page6">
        <img src="https://www.chilman.co.kr/data/editor/2411/52372d52063ee7aece26b382e036c44e_1730702973_7185.jpg" alt="page7">
        <img src="https://www.chilman.co.kr/data/editor/2411/52372d52063ee7aece26b382e036c44e_1730702973_866.jpg" alt="page8">
        <img src="https://www.chilman.co.kr/data/editor/2411/52372d52063ee7aece26b382e036c44e_1730702973_9754.jpg" alt="page9">
        <img src="https://www.chilman.co.kr/data/editor/2411/52372d52063ee7aece26b382e036c44e_1730702974_1008.jpg" alt="page10">
        <img src="https://www.chilman.co.kr/data/editor/2411/52372d52063ee7aece26b382e036c44e_1730702985_8739.jpg" alt="page11">
        <img src="https://www.chilman.co.kr/data/editor/2411/52372d52063ee7aece26b382e036c44e_1730702986_0281.jpg" alt="page12">
        <img src="https://www.chilman.co.kr/data/editor/2411/52372d52063ee7aece26b382e036c44e_1730702986_1411.jpg" alt="page13">
        <img src="https://www.chilman.co.kr/data/editor/2411/52372d52063ee7aece26b382e036c44e_1730702986_3633.jpg" alt="page14">
        <img src="https://www.chilman.co.kr/data/editor/2411/52372d52063ee7aece26b382e036c44e_1730702986_4995.jpg" alt="page15">
        <img src="https://www.chilman.co.kr/data/editor/2411/52372d52063ee7aece26b382e036c44e_1730702986_5984.jpg" alt="page16">
        
        <div class="navigation">
            <div class="nav-button" onclick="prevPage()">이전</div>
            <div class="nav-button" onclick="nextPage()">다음</div>
        </div>
    </div>

    <script>
        let currentIndex = 0;
        const images = document.querySelectorAll(".flipbook img");

        function showPage(index) {
            images.forEach(img => img.classList.remove("active"));
            images[index].classList.add("active");
        }

        function prevPage() {
            currentIndex = (currentIndex === 0) ? images.length - 1 : currentIndex - 1;
            showPage(currentIndex);
        }

        function nextPage() {
            currentIndex = (currentIndex === images.length - 1) ? 0 : currentIndex + 1;
            showPage(currentIndex);
        }
    </script>
</body>
</html>
