<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>2026 Seyoung Invitational 2026</title>

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Arial',sans-serif;
}

body{
background:#0f0f0f;
color:white;
display:flex;
justify-content:center;
align-items:center;
min-height:100vh;
padding:20px;
}

.container{
max-width:500px;
width:100%;
text-align:center;
}

h1{
color:#d4af37;
margin-bottom:10px;
}

.subtitle{
margin-bottom:25px;
color:#ccc;
}

input{
width:100%;
padding:14px;
margin-bottom:10px;
border:none;
border-radius:10px;
font-size:16px;
}

.checkbox{
margin:15px 0;
font-size:14px;
}

#wheel-container{
position:relative;
width:320px;
height:320px;
margin:20px auto;
}

#wheel{
width:320px;
height:320px;
border-radius:50%;
border:8px solid #d4af37;
transition:transform 6s cubic-bezier(0.17,0.67,0.12,0.99);

background:
conic-gradient(
#d4af37 0deg 72deg,
#1f1f1f 72deg 144deg,
#d4af37 144deg 216deg,
#1f1f1f 216deg 288deg,
#d4af37 288deg 360deg
);
}

.pointer{
position:absolute;
top:-15px;
left:50%;
transform:translateX(-50%);
font-size:40px;
z-index:10;
}

button{
width:100%;
padding:15px;
font-size:18px;
font-weight:bold;
background:#d4af37;
color:black;
border:none;
border-radius:10px;
cursor:pointer;
}

button:hover{
opacity:0.9;
}

#result{
margin-top:25px;
font-size:24px;
font-weight:bold;
color:#d4af37;
}
</style>
</head>

<body>

<div class="container">

<h1>2026 Seyoung Invitational 2026</h1>
<p class="subtitle">Lucky Roulette Event</p>

<input type="text" id="name" placeholder="이름 입력">

<input type="tel" id="phone" placeholder="연락처 입력">

<div class="checkbox">
<label>
<input type="checkbox" id="agree">
본 이벤트 참여를 위해 이름 및 연락처 수집에 동의합니다.
</label>
</div>

<div id="wheel-container">

<div class="pointer">▼</div>

<div id="wheel"></div>

</div>

<button onclick="spinWheel()">룰렛 돌리기</button>

<div id="result"></div>

</div>

<script>

let spinning=false;

const prizes=[
"드라이버",
"캐디백",
"캐디백",
"볼케이스",
"볼케이스",
"볼케이스",
"볼케이스",
"볼케이스",
"볼케이스",
"볼케이스",
"볼케이스",
"볼케이스",
"볼케이스",
"골프공",
"골프공",
"골프공",
"골프공",
"골프공",
"골프공",
"골프공",
"골프공",
"골프공",
"골프공",
"골프공",
"골프공",
"골프공",
"골프공",
"골프공",
"골프공",
"골프공",
"골프공",
"골프공",
"골프공",
"꽝",
"꽝",
"꽝",
"꽝",
"꽝",
"꽝",
"꽝",
"꽝",
"꽝",
"꽝",
"꽝",
"꽝",
"꽝",
"꽝",
"꽝"
];

function spinWheel(){

if(spinning) return;

const name=document.getElementById("name").value;
const phone=document.getElementById("phone").value;
const agree=document.getElementById("agree").checked;

if(name===""){
alert("이름을 입력해주세요.");
return;
}

if(phone===""){
alert("연락처를 입력해주세요.");
return;
}

if(!agree){
alert("개인정보 수집 동의가 필요합니다.");
return;
}

spinning=true;

const wheel=document.getElementById("wheel");

const randomIndex=Math.floor(Math.random()*prizes.length);

const prize=prizes[randomIndex];

const rotation=360*8+Math.floor(Math.random()*360);

wheel.style.transform=`rotate(${rotation}deg)`;

setTimeout(()=>{

document.getElementById("result").innerHTML=
`🎉 당첨 결과 : ${prize}`;

spinning=false;

},6000);

}

</script>

</body>
</html>
