<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For My Valentine 💖</title>

<style>
    body {
        margin: 0;
        padding: 0;
        font-family: 'Segoe UI', sans-serif;
        background: black;
        overflow: hidden;
        color: white;
        text-align: center;
    }

    /* Animated background */
    .hearts {
        position: fixed;
        width: 100%;
        height: 100%;
        overflow: hidden;
        z-index: -1;
    }

    .hearts span {
        position: absolute;
        display: block;
        color: pink;
        animation: float 10s linear infinite;
        font-size: 20px;
    }

    @keyframes float {
        0% { transform: translateY(100vh) scale(1); opacity: 1; }
        100% { transform: translateY(-10vh) scale(1.5); opacity: 0; }
    }

    h1 {
        font-size: 45px;
        margin-top: 60px;
        animation: fadeIn 3s ease-in-out;
    }

    @keyframes fadeIn {
        from { opacity: 0; }
        to { opacity: 1; }
    }

    img {
        width: 250px;
        border-radius: 20px;
        margin: 20px 0;
        box-shadow: 0 0 30px pink;
    }

    .btn {
        padding: 15px 30px;
        font-size: 18px;
        margin: 20px;
        border: none;
        border-radius: 30px;
        cursor: pointer;
        transition: 0.3s;
    }

    .yes {
        background: hotpink;
        color: white;
    }

    .yes:hover {
        transform: scale(1.1);
        background: deeppink;
    }

    .no {
        background: white;
        color: hotpink;
        position: absolute;
    }

    #message {
        font-size: 26px;
        margin-top: 20px;
        font-weight: bold;
        color: pink;
    }
</style>
</head>

<body>

<!-- Background Hearts -->
<div class="hearts">
    <script>
        for (let i = 0; i < 30; i++) {
            document.write("<span style='left:" + Math.random()*100 + "%; animation-duration:" + (5+Math.random()*5) + "s;'>💖</span>");
        }
    </script>
</div>

<!-- Background Music -->
<audio autoplay loop>
    <!-- Replace with your romantic song link -->
    <source src="your-song.mp3" type="audio/mpeg">
</audio>

<h1>💘 Emily, Will You Be My Valentine? 💘</h1>

<!-- Replace with your picture -->
<img src="your-photo.jpg" alt="Our Photo">

<p>You are my favorite person, my happiness, and my forever. ✨</p>

<button class="btn yes" onclick="sayYes()">Yes, of course! ❤️</button>
<button class="btn no" onmouseover="moveNo()" id="noBtn">No 😜</button>

<div id="message"></div>

<script>
function sayYes() {
    document.getElementById("message").innerHTML =
        "YAY!!! 💕 I love you so much! Can't wait for our special day! 💍💖";
}

function moveNo() {
    var btn = document.getElementById("noBtn");
    btn.style.left = Math.random() * (window.innerWidth - 100) + "px";
    btn.style.top = Math.random() * (window.innerHeight - 50) + "px";
}
</script>

</body>
</html>
