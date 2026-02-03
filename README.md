<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Lafin | Backend Engineer</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

<style>
:root{
--bg:#0b0f1a;
--text:#e5e7eb;
--accent:#38bdf8;
--card:rgba(255,255,255,0.08);
}

.light{
--bg:#f4f7fb;
--text:#111;
--card:rgba(0,0,0,0.05);
--accent:#2563eb;
}

body{
margin:0;
font-family:Poppins;
background:var(--bg);
color:var(--text);
overflow-x:hidden;
}

/* PARTICLES */
canvas{
position:fixed;
top:0;
left:0;
z-index:-1;
}

/* HERO */
.hero{
text-align:center;
padding:80px 20px;
}

.hero img{
width:140px;
border-radius:50%;
border:3px solid var(--accent);
}

h1{
font-size:48px;
margin:10px 0;
}

.btn{
background:var(--accent);
border:none;
padding:12px 20px;
border-radius:10px;
color:white;
cursor:pointer;
font-weight:600;
}

/* CARDS */
.container{
max-width:1000px;
margin:auto;
padding:20px;
}

.card{
background:var(--card);
backdrop-filter:blur(14px);
padding:25px;
border-radius:16px;
margin:25px 0;
opacity:0;
transform:translateY(30px);
transition:0.6s;
}

.card.show{
opacity:1;
transform:translateY(0);
}

/* TIMELINE */
.timeline{
border-left:3px solid var(--accent);
padding-left:20px;
}

.tag{
display:inline-block;
background:var(--accent);
padding:6px 12px;
border-radius:20px;
margin:5px;
font-size:14px;
}

a{
color:var(--accent);
text-decoration:none;
}

footer{
text-align:center;
opacity:0.6;
padding:30px;
}
</style>
</head>

<body>

<canvas id="bg"></canvas>

<section class="hero">
<img src="profile.png">
<h1>Felipe <span style="color:var(--accent)">Lafin</span></h1>
<h3>Full Stack Developer JR</h3>
<p>Java | C# | Spring Boot | Java Script | HTML | CSS | Angular | Typescript | Python | SQL | Studying React</p>

<button class="btn" onclick="toggleMode()">Toggle Theme</button>

<p>
<a href="https://github.com/FelipeLafin">GitHub</a> |
<a href="https://www.linkedin.com/in/felipe-lafin-haushahn-3785a2237/">LinkedIn</a>
</p>
</section>

<div class="container">

<div class="card">
<h2>🚀 Sobre Mim</h2>
<p>
Sou estudante de Ciências da Computação e entusiasta da tecnologia. Estou no quinto semestre do curso e em constante aprendizado sobre programação e desenvolvimento.

Tenho facilidade em trabalhar em equipe, sou comunicativo, proativo, focado e sempre busco expandir minhas habilidades. Desde 2016, participo do movimento escoteiro, onde desenvolvi competências como liderança, organização e resiliência, aplicáveis tanto na vida pessoal quanto profissional.

Estou em busca de oportunidades para aplicar meu conhecimento e contribuir com entusiasmo para o sucesso de projetos e equipes.

Segue meu portfólio no github:
https://github.com/FelipeLafin

</p>
</div>

<div class="card">
<h2>💼 Experiência</h2>

<div class="timeline">
<h3>Grupo Panvel</h3>
<b>Estagiário - Atual</b>
<ul>
<li>APIs REST com Spring Boot</li>
<li>SQL</li>
<li>PostgreSQL</li>
<li>Metodologia Ágile</li>
<li>Java</li>
<li>Docker</li>
</ul>
</div>

<div class="timeline">
<h3>Ifood</h3>
<b>Entregador - 2022/2024</b>
<ul>
<li>Comunicação com cliente</li>
</ul>
</div>

<div class="timeline">
<h3>Villela Brasil Bank</h3>
<b>Desenvolvedor Full Stack JR</b>
<ul>
<li>C#</li>
<li>SQL</li>
<li>React</li>
<li>Metodologia Ágile</li>
<li>TypeScript</li>
<li>Angular</li>
<li>HTML</li>
<li>SCSS</li>
<li>JavaScript</li>
</ul>
</div>
</div>

<div class="card">
<div>
<h2>📌 Projetos</h2>

<h3>Exercício de gestão de contas bancárias</h3>
<p>Gestão de pedidos, usuários e cardápio.</p>
<b>Stack:</b> Java • Spring Boot • PostgreSQL
<br><br>
<a href="https://github.com/FelipeLafin/gestao-contas-bancarias">Ver Projeto</a>
</div>

<div>
<h3>Software Cripto Market</h3>
<p>Este aplicativo permite acompanhar o preço das criptomoedas mais importantes, simular o valor que seria recebido/pago baseado no valor em tempo real da criptomoeda selecionada e redirecionar o usuário para a aba de compra/venda no site oficial.</p>
<b>Stack:</b> Python
<br><br>
<a href="https://github.com/FelipeLafin/Software_Cripto_Market">Ver Projeto</a>
</div>
<div>
<h3>Mais projetos:</h3>
<a href="https://github.com/FelipeLafin?tab=repositories">Ver mais projetos</a>
</div>

<div class="card">
<h2>🧠 Skills</h2>
<span class="tag">Java</span>
<span class="tag">C#</span>
<span class="tag">Spring Boot</span>
<span class="tag">SQL</span>
<span class="tag">Java Script</span>
<span class="tag">HTML</span>
<span class="tag">CSS</span>
<span class="tag">Angular</span>
<span class="tag">Typescript</span>
<span class="tag">Python</span>
<span class="tag">React</span>
</div>

<div class="card">
<h2>🎓 Educação</h2>
<p>Faculdade: ATITUS Educação (Campus Mont Serra't)</p>
<p>Curso: Ciências da Computação - Bacharel</p>
<p>Semestre Atual: 5º</p>
</div>

</div>

<footer>
© 2026 Felipe Lafin
</footer>

<script>
/* DARK MODE */
function toggleMode(){
document.body.classList.toggle("light");
}

/* SCROLL ANIMATION */
const cards=document.querySelectorAll(".card");
window.addEventListener("scroll",()=>{
cards.forEach(c=>{
const top=c.getBoundingClientRect().top;
if(top<window.innerHeight-50){
c.classList.add("show");
}
});
});

/* PARTICLES */
const canvas=document.getElementById("bg");
const ctx=canvas.getContext("2d");
canvas.width=window.innerWidth;
canvas.height=window.innerHeight;

let particles=[];
for(let i=0;i<80;i++){
particles.push({
x:Math.random()*canvas.width,
y:Math.random()*canvas.height,
r:Math.random()*2,
dx:(Math.random()-0.5),
dy:(Math.random()-0.5)
});
}

function animate(){
ctx.clearRect(0,0,canvas.width,canvas.height);
particles.forEach(p=>{
ctx.beginPath();
ctx.arc(p.x,p.y,p.r,0,Math.PI*2);
ctx.fillStyle="#38bdf8";
ctx.fill();
p.x+=p.dx;
p.y+=p.dy;
if(p.x<0||p.x>canvas.width) p.dx*=-1;
if(p.y<0||p.y>canvas.height) p.dy*=-1;
});
requestAnimationFrame(animate);
}
animate();
</script>
