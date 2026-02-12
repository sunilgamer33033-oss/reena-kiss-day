# reena-kiss-day
This is a small surprise for my Meri Pyari Bhatakti Aatma Reena ❤️   A password protected romantic page made specially for Kiss Day 💋   Made with pure love and feelings 💖
<!DOCTYPE html>
<html>
<head>
    <title>Secret For Reena 💋</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
            background: linear-gradient(45deg, #ff416c, #ff4b2b);
            text-align: center;
            color: white;
            overflow: hidden;
        }

        #lockScreen {
            margin-top: 40%;
        }

        input {
            padding: 10px;
            font-size: 18px;
            border-radius: 20px;
            border: none;
            text-align: center;
        }

        button {
            padding: 10px 20px;
            font-size: 18px;
            border-radius: 20px;
            border: none;
            margin-top: 10px;
            cursor: pointer;
        }

        #content {
            display: none;
            padding-top: 30px;
        }

        img {
            width: 80%;
            max-width: 300px;
            border-radius: 20px;
            margin-top: 15px;
            box-shadow: 0 0 20px white;
        }

        .heart {
            position: absolute;
            font-size: 20px;
            animation: fall linear infinite;
            color: pink;
        }

        @keyframes fall {
            0% { top: -10%; }
            100% { top: 100%; }
        }
    </style>
</head>
<body>

<div id="lockScreen">
    <h2>Enter Password 💕</h2>
    <input type="password" id="pass" placeholder="Enter password">
    <br>
    <button onclick="checkPass()">Open 💌</button>
</div>

<div id="content">
    <h1>Happy Kiss Day Reena 💋</h1>
    <p>Meri Pyari Bhatakti Aatma ❤️</p>
    <p>Tum meri duniya ho 💖</p>

    <img src="photo.jpg" alt="Our Photo">

</div>

<script>
    function checkPass() {
        var password = document.getElementById("pass").value;
        if(password === "kiss") {
            document.getElementById("lockScreen").style.display = "none";
            document.getElementById("content").style.display = "block";
            startHearts();
        } else {
            alert("Wrong Password ❌");
        }
    }

    function startHearts() {
        setInterval(function() {
            const heart = document.createElement("div");
            heart.classList.add("heart");
            heart.innerHTML = "❤️";
            heart.style.left = Math.random() * 100 + "vw";
            heart.style.animationDuration = (Math.random() * 3 + 2) + "s";
            document.body.appendChild(heart);

            setTimeout(() => {
                heart.remove();
            }, 5000);
        }, 300);
    }
</script>

</body>
</html>
