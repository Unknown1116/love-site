<!DOCTYPE html>  
<html lang="en">  
<head>  
<meta charset="UTF-8">  
<title>For You 💕</title>  
<meta name="viewport" content="width=device-width, initial-scale=1.0">  
  
<style>  
body {  
    margin: 0;  
    height: 100vh;  
    background: linear-gradient(135deg, #ffb6c1, #ffdde1);  
    font-family: "Georgia", serif;  
    color: #fff;  
    display: flex;  
    align-items: center;  
    justify-content: center;  
    overflow: hidden;  
}  
  
.page {  
    display: none;  
    text-align: center;  
    max-width: 90%;  
    animation: fade 1s ease;  
}  
  
.active {  
    display: block;  
}  
  
h1, h2, p {  
    text-shadow: 0 2px 5px rgba(0,0,0,0.2);  
}  
  
button {  
    background: rgba(255,255,255,0.9);  
    color: #ff4f7b;  
    border: none;  
    border-radius: 30px;  
    padding: 12px 28px;  
    font-size: 18px;  
    margin: 12px;  
    cursor: pointer;  
    transition: 0.3s ease;  
}  
  
button:hover {  
    transform: scale(1.08);  
}  
  
@keyframes fade {  
    from { opacity: 0; transform: translateY(20px); }  
    to { opacity: 1; transform: translateY(0); }  
}  
  
.heart {  
    position: absolute;  
    bottom: -20px;  
    font-size: 20px;  
    animation: floatUp 8s linear infinite;  
    opacity: 0.6;  
}  
  
@keyframes floatUp {  
    from { transform: translateY(0); }  
    to { transform: translateY(-110vh); }  
}  
</style>  
</head>  
  
<body>  
  
<!-- PAGE 1 -->  
<div id="page1" class="page active">  
    <h1>Hey you… 💕</h1>  
    <p>  
        I’ve been thinking about this for a while now.<br><br>  
        Not because I was unsure…<br>  
        but because I wanted to ask you in a way that actually feels special.<br><br>  
        You’re not just someone I talk to.<br>  
        You’re someone who makes my days better without even trying.<br><br>  
        And before I ask you something important…<br>  
        there’s something I need to know first.  
    </p>  
    <button onclick="nextPage(2)">Continue</button>  
</div>  
  
<!-- PAGE 2 -->  
<div id="page2" class="page">  
    <h2>Be honest with me 🤍</h2>  
    <p>  
        When you think about us…<br>  
        do you feel that spark?<br>  
        That connection?<br><br>  
        Because I know in my heart<br>  
        I’ve fallen for you.  
    </p>  
    <button onclick="nextPage(4)">Yes</button>  
    <button onclick="nextPage(3)">No</button>  
</div>  
  
<!-- PAGE 3 -->  
<div id="page3" class="page">  
    <h2>Hmm… 🥺</h2>  
    <p>  
        That doesn’t quite match the way you look at me.<br><br>  
        Or the way you make me feel.<br><br>  
        Take a second…<br>  
        and answer from your heart.  
    </p>  
    <button id="yesGrow" onclick="nextPage(4)">Yes</button>  
    <button onclick="growYes()">No</button>  
</div>  
  
<!-- PAGE 4 -->  
<div id="page4" class="page">  
    <h2>You should know something 👑</h2>  
    <p>  
        You’ve never just been “anyone” to me.<br><br>  
        You’re the girl I smile about randomly.<br>  
        The one I think about at night.<br>  
        The one who somehow feels different from everyone else.<br><br>  
        To me… you’ve always been my princess.  
    </p>  
    <button onclick="nextPage(5)">Yes</button>  
    <button onclick="autoYes()">No</button>  
</div>  
  
<!-- PAGE 5 -->  
<div id="page5" class="page">  
    <h2>Okay… deep breath 💖</h2>  
    <p>  
        So here it is.<br><br>  
        Sidane Douglas…<br><br>  
        I don’t just want moments with you.<br>  
        I don’t just want “vibes.”<br><br>  
        I want something real.<br>  
        Something intentional.<br>  
        Something we can grow.<br><br>  
        Will you be my girlfriend?  
    </p>  
    <button onclick="nextPage(6)">Yes</button>  
    <button onclick="nextPage(6)">Yes</button>  
</div>  
  
<!-- PAGE 6 -->  
<div id="page6" class="page">  
    <h1>🎉 It’s Official 🎉</h1>  
    <h2>You’re mine and I’m yours 💕</h2>  
    <p>  
        I promise to appreciate you.<br>  
        To respect you.<br>  
        To choose you — not just today, but every day.<br><br>  
        Thank you for trusting me with your heart.<br><br>  
        You make my life brighter just by being in it.<br><br>  
        I love you ❤️  
    </p>  
</div>  
  
<script>  
function nextPage(num) {  
    document.querySelectorAll(".page").forEach(p => p.classList.remove("active"));  
    document.getElementById("page" + num).classList.add("active");  
}  
  
function growYes() {  
    const btn = document.getElementById("yesGrow");  
    let size = parseInt(window.getComputedStyle(btn).fontSize);  
    btn.style.fontSize = (size + 10) + "px";  
}  
  
function autoYes() {  
    alert("I’ll take that as a yes… because I already know 💕");  
    nextPage(5);  
}  
  
setInterval(() => {  
    const heart = document.createElement("div");  
    heart.className = "heart";  
    heart.innerHTML = "❤️";  
    heart.style.left = Math.random() * 100 + "vw";  
    heart.style.animationDuration = (6 + Math.random() * 4) + "s";  
    document.body.appendChild(heart);  
    setTimeout(() => heart.remove(), 8000);  
}, 700);  
</script>  
  
</body>  
</html>  
