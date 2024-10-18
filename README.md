<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Video Player</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #000;
            margin: 0;
        }
        video {
            width: 80%;
            max-width: 1000px;
            border: 2px solid #fff;
            border-radius: 10px;
        }
        #fullscreenBtn {
            position: absolute;
            top: 10px;
            right: 10px;
            background-color: rgba(0, 0, 0, 0.5);
            color: #fff;
            border: none;
            padding: 10px;
            cursor: pointer;
            border-radius: 5px;
            font-size: 16px;
        }
    </style>
</head>
<body>
    <video id="myVideo" controls>
        <source src="https://pullzonetaher.b-cdn.net/stream/001/1/Osman%20S06%20003%201080p.mp4" type="video/mp4">
        متصفحك لا يدعم تشغيل الفيديو
    </video>
    <button id="fullscreenBtn">ملء الشاشة</button>

    <script>
        const video = document.getElementById('myVideo');
        const fullscreenBtn = document.getElementById('fullscreenBtn');

        fullscreenBtn.addEventListener('click', () => {
            if (video.requestFullscreen) {
                video.requestFullscreen();
            } else if (video.webkitRequestFullscreen) { // Safari
                video.webkitRequestFullscreen();
            } else if (video.msRequestFullscreen) { // IE11
                video.msRequestFullscreen();
            }
        });
    </script>
</body>
</html>
