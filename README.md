<!DOCTYPE html>
<html>
<head>
<title>Happy One Month 🎀</title>
<style> #opening{
text-align:center;
margin-top:100px;
}

.envelope{
font-size:90px;
animation:float 2s ease-in-out infinite;
}

#opening h2{
color:#ff4081;
font-size:28px;
}

#opening p{
font-size:18px;
color:#d81b60;
}

#opening button{
background:#ff4081;
color:white;
}

@keyframes float{
0%,100%{
transform:translateY(0);
}
50%{
transform:translateY(-12px);
}
}
body{
background:#ffd6e7;
font-family:Arial,sans-serif;
text-align:center;
padding:50px;
overflow:hidden;
}

h1{
color:#ff4081;
}

button{
padding:15px 30px;
font-size:18px;
border:none;
border-radius:20px;
cursor:pointer;
margin:10px;
}

#yes{
background:#ff4081;
color:white;
}

#no{
background:#ffffff;
}

#message{
display:none;
margin-top:30px;
font-size:22px;
color:#d81b60;
}

.heart{
position:fixed;
font-size:20px;
animation:fall 6s linear infinite;
}

@keyframes fall{
from{
transform:translateY(-100px);
}
to{
transform:translateY(110vh);
}
}
</style>
</head>

<body>

<div id="opening">
    <div class="envelope">💌</div>
    <h2>A little something for you ❤️</h2>

   <p>Open this when you're ready...</p>
  <button onclick="openGift()">Open Me 💗</button>
</div>

<div id="main" style="display:none;">
    <h1>Happy One Month ❤️</h1>
    <p>
    To the person who somehow became one of my favorite parts of every day.
    </p>

   <p>
    Click a button ↓
    </p>

   <button id="yes" onclick="showMessage()">
    Open Gift
    </button>

   <button id="no">
    Definitely Not The Gift
    </button>
    <div id="message">
    💗 Happy One Month 💗
    <br><br>
    Thank you for being my cupcake scented Saboona.
    I love you so much
    <br><br>
    I’m gonna steal you and put you in my bag.
    </div>

</div>

<script>
function showMessage(){
document.getElementById("message").style.display="block";
}
function openGift(){
document.getElementById("opening").style.display="none";
document.getElementById("main").style.display="block";
}
const noButton=document.getElementById("no");

noButton.addEventListener("mouseover",()=>{
const x=Math.random()*(window.innerWidth-150);
const y=Math.random()*(window.innerHeight-100);
noButton.style.position="absolute";
noButton.style.left=x+"px";
noButton.style.top=y+"px";
});

setInterval(()=>{
const heart=document.createElement("div");
heart.classList.add("heart");
heart.innerHTML="❤️";
heart.style.left=Math.random()*100+"vw";
document.body.appendChild(heart);

setTimeout(()=>{
heart.remove();
},6000);
},500);
</script>

</body>
</html>
