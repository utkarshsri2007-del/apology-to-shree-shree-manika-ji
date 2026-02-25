<!DOCTYPE html>
<html>
<head>
<title>Apology 💛</title>
<style>
body {
    margin: 0;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    background: linear-gradient(-45deg, #ff9a9e, #fad0c4, #fbc2eb, #a6c1ee);
    background-size: 400% 400%;
    animation: gradientBG 8s ease infinite;
    font-family: 'Segoe UI', sans-serif;
    overflow: hidden;
}

@keyframes gradientBG {
    0% {background-position: 0% 50%;}
    50% {background-position: 100% 50%;}
    100% {background-position: 0% 50%;}
}

.card {
    background: rgba(255,255,255,0.9);
    padding: 50px;
    border-radius: 25px;
    box-shadow: 0 15px 40px rgba(0,0,0,0.2);
    text-align: center;
    animation: fadeIn 2s ease-in-out;
}

h1 {
    color: #ff4d6d;
    animation: slideDown 1.5s ease;
}

p {
    font-size: 20px;
    font-style: italic;
    color: #444;
    animation: fadeInText 3s ease;
}

@keyframes fadeIn {
    from {opacity:0; transform: scale(0.8);}
    to {opacity:1; transform: scale(1);}
}

@keyframes slideDown {
    from {opacity:0; transform: translateY(-30px);}
    to {opacity:1; transform: translateY(0);}
}

@keyframes fadeInText {
    from {opacity:0;}
    to {opacity:1;}
}

/* Floating hearts */
.heart {
    position: absolute;
    bottom: -20px;
    font-size: 20px;
    animation: floatUp 6s linear infinite;
}

@keyframes floatUp {
    0% {transform: translateY(0); opacity:1;}
    100% {transform: translateY(-110vh); opacity:0;}
}
</style>
</head>
<body>

<div class="card">
    <h1>Kahe khafa aise chulbul si bulbul 💛</h1>
    <p>Kahe nahin tu maane batiya re… ✨</p>
</div>

<script>
function createHeart() {
    const heart = document.createElement("div");
    heart.classList.add("heart");
    heart.innerHTML = "💛";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.fontSize = (Math.random() * 20 + 15) + "px";
    heart.style.animationDuration = (Math.random() * 3 + 3) + "s";
    document.body.appendChild(heart);

    setTimeout(() => {
        heart.remove();
    }, 6000);
}

setInterval(createHeart, 500);
</script>

</body>
</html>
