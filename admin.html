let balance=parseFloat(localStorage.getItem("bal")||1000)
let matches=JSON.parse(localStorage.getItem("matches")||"[]")
let bets=JSON.parse(localStorage.getItem("bets")||"[]")

function save(){
localStorage.setItem("bal",balance)
localStorage.setItem("matches",JSON.stringify(matches))
localStorage.setItem("bets",JSON.stringify(bets))
}

// ================= USER PAGE =================
if(document.getElementById("matchList")){

document.getElementById("balanceBox").innerText="Balance: "+balance

renderMatches()
renderHistory()

window.bet=function(){

let idx=document.querySelector('input[name="m"]:checked')
if(!idx) return alert("เลือกคู่ก่อน")

idx=idx.value
let pick=prompt("พิมพ์ A หรือ B").toUpperCase()
let stake=parseFloat(document.getElementById("stake").value)

if(stake>balance) return alert("เครดิตไม่พอ")

balance-=stake

bets.push({
matchId:idx,
match:matches[idx].a+" vs "+matches[idx].b,
pick:pick,
stake:stake,
odds:1.8,
status:"Pending",
profit:0
})

save()
location.reload()
}
}

// ================= ADMIN PAGE =================
if(document.getElementById("adminMatches")){

renderAdmin()

window.addMatch=function(){
matches.push({
a:document.getElementById("a").value,
b:document.getElementById("b").value,
score:"",
result:"Pending"
})
save()
location.reload()
}

window.setResult=function(i){

let score=prompt("ใส่สกอร์ เช่น 2-1")
let winner=prompt("ผลการแข่งขัน A / B / D(เสมอ)").toUpperCase()

matches[i].score=score
matches[i].result=winner

// ===== คำนวณผลทุกบิล =====
bets.forEach(b=>{

if(b.matchId==i && b.status=="Pending"){

if(winner=="D"){
b.status="Draw"
balance+=b.stake // คืนเงิน
}
else if(b.pick==winner){
b.status="Win"
b.profit=b.stake*b.odds
balance+=b.profit
}
else{
b.status="Lose"
}

}
})

save()
alert("อัปเดตผลเรียบร้อย")
location.reload()
}
}

// ================= FUNCTIONS =================
function renderMatches(){
let html=""
matches.forEach((m,i)=>{
html+=`
<input type="radio" name="m" value="${i}">
${m.a} vs ${m.b}
(${m.result=="Pending"?"ยังไม่แข่ง":"ผล: "+m.score})
<br>`
})
document.getElementById("matchList").innerHTML=html
}

function renderHistory(){
let h=""
bets.forEach(b=>{
h+=`
<tr>
<td>${b.match}</td>
<td>${b.pick}</td>
<td>${b.stake}</td>
<td>${b.status}</td>
<td>${b.profit}</td>
</tr>`
})
document.getElementById("history").innerHTML=h
}

function renderAdmin(){
let html=""
matches.forEach((m,i)=>{
html+=`
<div>
${m.a} vs ${m.b}
(ผล: ${m.result=="Pending"?"ยังไม่แข่ง":m.score})
<button onclick="setResult(${i})">เฉลยผล</button>
</div><br>`
})
document.getElementById("adminMatches").innerHTML=html
}
