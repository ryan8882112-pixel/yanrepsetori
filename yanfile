<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<title>PayX Payment Store</title>

<style>
*{box-sizing:border-box;margin:0;padding:0;font-family:Arial,sans-serif}

body{
background:#070a12;
color:#fff;
min-height:100vh;
background-image:
radial-gradient(circle at 10% 10%,#211b55 0,transparent 30%),
radial-gradient(circle at 90% 20%,#073c50 0,transparent 30%);
}

.hidden{display:none!important}

header{
position:sticky;
top:0;
z-index:100;
padding:15px 5%;
display:flex;
align-items:center;
justify-content:space-between;
background:#080b14dd;
backdrop-filter:blur(15px);
border-bottom:1px solid #252b3d;
}

.logo{
font-size:25px;
font-weight:900;
}

.logo span{
background:linear-gradient(90deg,#7c5cff,#00e5ff);
-webkit-background-clip:text;
color:transparent;
}

nav{
display:flex;
gap:5px;
flex-wrap:wrap;
}

nav button{
background:none;
border:0;
color:#aeb5c7;
padding:9px 11px;
border-radius:9px;
cursor:pointer;
}

nav button:hover{
background:#191e2e;
color:#fff;
}

.container{
width:92%;
max-width:1150px;
margin:30px auto;
}

.btn{
border:0;
border-radius:11px;
padding:12px 17px;
cursor:pointer;
font-weight:bold;
color:white;
background:linear-gradient(135deg,#7657ff,#367cff);
}

.btn:hover{opacity:.88}
.btn.green{background:linear-gradient(135deg,#00a76b,#19d78c)}
.btn.red{background:linear-gradient(135deg,#d82f4e,#ff536e)}
.btn.orange{background:linear-gradient(135deg,#d47b00,#ffb52c)}
.btn.full{width:100%;margin-top:8px}

input,textarea{
width:100%;
padding:13px;
margin:6px 0;
border-radius:10px;
border:1px solid #30374b;
background:#090d17;
color:#fff;
outline:none;
}

input:focus,textarea:focus{
border-color:#795bff;
}

.auth{
width:92%;
max-width:420px;
margin:70px auto;
padding:30px;
border:1px solid #292f43;
border-radius:23px;
background:#111625;
box-shadow:0 25px 80px #0009;
}

.auth-logo{
text-align:center;
font-size:32px;
font-weight:900;
margin-bottom:20px;
}

.auth-logo span{
background:linear-gradient(90deg,#7c5cff,#00e5ff);
-webkit-background-clip:text;
color:transparent;
}

.auth h2{text-align:center;margin-bottom:15px}

.switch{
text-align:center;
color:#8a91a5;
margin-top:15px;
cursor:pointer;
}

.switch:hover{color:#00e5ff}

.hero{
text-align:center;
padding:35px 10px 25px;
}

.hero h1{
font-size:43px;
margin-bottom:10px;
}

.gradient{
background:linear-gradient(90deg,#7c5cff,#00e5ff);
-webkit-background-clip:text;
color:transparent;
}

.hero p{color:#8d95a8}

/* BANNER */

.banner-area{
position:relative;
width:100%;
overflow:hidden;
border-radius:22px;
margin-bottom:30px;
border:1px solid #292f43;
}

.banner-track{
display:flex;
transition:.5s ease;
}

.banner{
min-width:100%;
height:270px;
position:relative;
background-size:cover;
background-position:center;
display:flex;
align-items:flex-end;
}

.banner::after{
content:"";
position:absolute;
inset:0;
background:linear-gradient(transparent 25%,#000d);
}

.banner-content{
position:relative;
z-index:2;
padding:28px;
max-width:650px;
}

.banner-content h2{
font-size:30px;
margin-bottom:8px;
}

.banner-content p{
color:#ddd;
}

.banner-dots{
position:absolute;
z-index:5;
bottom:12px;
right:18px;
display:flex;
gap:6px;
}

.dot{
width:8px;
height:8px;
border-radius:50%;
background:#777;
}

.dot.active{background:#fff}

/* PRODUCTS */

.grid{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
gap:20px;
}

.card{
overflow:hidden;
background:#111625;
border:1px solid #292f43;
border-radius:19px;
transition:.25s;
}

.card:hover{
transform:translateY(-5px);
border-color:#765bff;
box-shadow:0 15px 45px #0008;
}

.product-image{
width:100%;
height:170px;
object-fit:cover;
background:#181d2b;
}

.product-content{
padding:19px;
}

.product-content h3{margin-bottom:8px}

.price{
color:#00e5ff;
font-size:21px;
font-weight:900;
margin:10px 0;
}

.stock{
font-size:13px;
color:#50e39a;
margin-bottom:14px;
}

.stock.empty{color:#ff5e78}

.product-content .btn{width:100%}

/* TABLE */

.table-wrap{
overflow:auto;
border:1px solid #292f43;
border-radius:17px;
}

table{
width:100%;
min-width:750px;
border-collapse:collapse;
background:#111625;
}

th,td{
padding:14px;
border-bottom:1px solid #272d40;
text-align:left;
}

th{
background:#0e1320;
color:#00e5ff;
}

.status{
display:inline-block;
padding:6px 10px;
border-radius:20px;
font-size:12px;
font-weight:bold;
background:#d89c1830;
color:#ffc34c;
}

.status.success{
background:#18b86a30;
color:#48e69a;
}

.status.rejected{
background:#ef405030;
color:#ff7185;
}

/* PAYMENT */

.qris-box{
width:92%;
max-width:510px;
margin:40px auto;
text-align:center;
padding:30px;
background:#111625;
border:1px solid #292f43;
border-radius:23px;
box-shadow:0 25px 70px #0008;
}

.qris{
width:270px;
height:270px;
object-fit:contain;
background:#fff;
padding:9px;
border-radius:14px;
margin:20px auto;
}

.total{
font-size:29px;
font-weight:900;
color:#00e5ff;
margin:15px;
}

.payment-info{
text-align:left;
padding:15px;
background:#090d17;
border:1px solid #292f43;
border-radius:12px;
line-height:1.8;
}

/* ADMIN */

.admin-tabs{
display:flex;
gap:8px;
flex-wrap:wrap;
margin:20px 0;
}

.admin-tabs button{
border:1px solid #30374b;
background:#111625;
color:#bbb;
padding:11px 15px;
border-radius:10px;
cursor:pointer;
}

.admin-tabs button:hover{
border-color:#765bff;
color:#fff;
}

.stats{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(180px,1fr));
gap:15px;
margin:20px 0;
}

.stat{
background:#111625;
border:1px solid #292f43;
border-radius:17px;
padding:20px;
}

.stat small{color:#858da0}
.stat h2{
margin-top:8px;
color:#00e5ff;
}

.admin-section{
margin-top:20px;
}

.admin-card{
background:#111625;
border:1px solid #292f43;
border-radius:17px;
padding:20px;
}

.admin-card img{
width:100%;
height:150px;
object-fit:cover;
border-radius:12px;
margin-bottom:12px;
}

.admin-card label{
display:block;
font-size:12px;
color:#8e95a8;
margin-top:7px;
}

/* MODAL */

.modal{
position:fixed;
inset:0;
z-index:999;
display:flex;
align-items:center;
justify-content:center;
background:#000b;
padding:20px;
}

.modal-box{
width:100%;
max-width:470px;
background:#111625;
border:1px solid #343c53;
border-radius:20px;
padding:28px;
}

.modal-box p{
color:#abb2c3;
line-height:1.7;
margin:12px 0 20px;
}

footer{
text-align:center;
color:#626a7d;
padding:45px 20px;
}

@media(max-width:650px){
header{padding:12px 3%}
.logo{font-size:20px}
nav button{font-size:10px;padding:7px}
.hero h1{font-size:31px}
.banner{height:220px}
.banner-content h2{font-size:23px}
}
</style>
</head>

<body>

<!-- LOGIN -->
<section id="loginPage">

<div class="auth">

<div class="auth-logo">
Pay<span>X</span>
</div>

<h2>🔐 Login Buyer</h2>

<input id="loginUser" placeholder="Username">
<input id="loginPass" type="password" placeholder="Password">

<button class="btn full" onclick="login()">Masuk</button>

<div class="switch" onclick="showRegister()">
Belum punya akun? Daftar
</div>

<div class="switch" onclick="showAdminLogin()">
👑 Login Admin
</div>

</div>
</section>


<!-- REGISTER -->
<section id="registerPage" class="hidden">

<div class="auth">

<div class="auth-logo">
Pay<span>X</span>
</div>

<h2>📝 Daftar Akun</h2>

<input id="regUser" placeholder="Username">
<input id="regPass" type="password" placeholder="Password">

<button class="btn full" onclick="register()">Daftar</button>

<div class="switch" onclick="showLogin()">
Sudah punya akun? Login
</div>

</div>
</section>


<!-- ADMIN LOGIN -->
<section id="adminLoginPage" class="hidden">

<div class="auth">

<div class="auth-logo">
Pay<span>X</span>
</div>

<h2>👑 Login Admin</h2>

<input id="adminUser" placeholder="Username Admin">
<input id="adminPass" type="password" placeholder="Password Admin">

<button class="btn full" onclick="adminLogin()">
Login Admin
</button>

<div class="switch" onclick="showLogin()">
← Kembali
</div>

</div>
</section>


<!-- BUYER STORE -->
<section id="storePage" class="hidden">

<header>

<div class="logo">Pay<span>X</span></div>

<nav>
<button onclick="showStore()">🏠 Beranda</button>
<button onclick="showTransactions()">📜 Transaksi</button>
<button onclick="logout()">Keluar</button>
</nav>

</header>

<div class="container">

<div class="hero">
<h1>Payment <span class="gradient">Store</span></h1>
<p>Belanja mudah dengan pembayaran QRIS.</p>
</div>

<!-- BANNER BUYER -->
<div class="banner-area">

<div id="bannerTrack" class="banner-track"></div>

<div id="bannerDots" class="banner-dots"></div>

</div>

<h2 style="margin-bottom:18px">🔥 Produk</h2>

<div id="productGrid" class="grid"></div>

</div>

<footer>
PayX Payment Store © 2026
</footer>

</section>


<!-- BUYER TRANSACTIONS -->
<section id="transactionPage" class="hidden">

<header>

<div class="logo">Pay<span>X</span></div>

<nav>
<button onclick="showStore()">🛍️ Produk</button>
<button onclick="showTransactions()">📜 Transaksi</button>
<button onclick="logout()">Keluar</button>
</nav>

</header>

<div class="container">

<h2>📜 Riwayat Transaksi</h2>

<br>

<div class="table-wrap">

<table>

<thead>
<tr>
<th>ID</th>
<th>Produk</th>
<th>Total</th>
<th>Tanggal</th>
<th>Status</th>
</tr>
</thead>

<tbody id="transactionList"></tbody>

</table>

</div>

</div>

</section>


<!-- PAYMENT -->
<section id="paymentPage" class="hidden">

<header>

<div class="logo">Pay<span>X</span></div>

<nav>
<button onclick="showStore()">← Kembali</button>
</nav>

</header>

<div class="container">

<div class="qris-box">

<h2>💳 Pembayaran QRIS</h2>

<div class="payment-info">

<div>
📦 Produk:
<b id="paymentProduct"></b>
</div>

<div>
💰 Total:
<b id="paymentTotal"></b>
</div>

</div>

<img
id="qrisImage"
class="qris"
src=""
alt="QRIS">

<p style="color:#888">
Scan QRIS menggunakan aplikasi pembayaran kamu.
</p>

<br>

<button class="btn green" onclick="confirmPayment()">
✅ Saya Sudah Bayar
</button>

</div>

</div>
</section>


<!-- ADMIN -->
<section id="adminPage" class="hidden">

<header>

<div class="logo">
Pay<span>X</span> ADMIN
</div>

<button class="btn red" onclick="adminLogout()">
Logout
</button>

</header>

<div class="container">

<h2>👑 Admin Panel</h2>

<div class="admin-tabs">

<button onclick="adminTab('dashboard')">
📊 Dashboard
</button>

<button onclick="adminTab('transactions')">
📋 Transaksi
</button>

<button onclick="adminTab('products')">
📦 Produk
</button>

<button onclick="adminTab('addproduct')">
➕ Tambah Produk
</button>

<button onclick="adminTab('banners')">
🖼️ Banner
</button>

<button onclick="adminTab('qris')">
💳 QRIS
</button>

</div>


<!-- DASHBOARD -->
<div id="adminDashboard" class="admin-section">

<div class="stats">

<div class="stat">
<small>Total Transaksi</small>
<h2 id="statTransactions">0</h2>
</div>

<div class="stat">
<small>Pending</small>
<h2 id="statPending">0</h2>
</div>

<div class="stat">
<small>Berhasil</small>
<h2 id="statSuccess">0</h2>
</div>

<div class="stat">
<small>Total Produk</small>
<h2 id="statProducts">0</h2>
</div>

<div class="stat">
<small>Total Nominal</small>
<h2 id="statNominal">Rp 0</h2>
</div>

</div>

</div>


<!-- TRANSACTIONS -->
<div id="adminTransactionsSection"
class="admin-section hidden">

<h2>📋 Transaksi</h2>

<br>

<div class="table-wrap">

<table>

<thead>
<tr>
<th>ID</th>
<th>User</th>
<th>Produk</th>
<th>Total</th>
<th>Tanggal</th>
<th>Status</th>
<th>Aksi</th>
</tr>
</thead>

<tbody id="adminTransactions"></tbody>

</table>

</div>

</div>


<!-- PRODUCTS -->
<div id="adminProductsSection"
class="admin-section hidden">

<h2>📦 Kelola Produk</h2>

<br>

<div id="adminProductGrid" class="grid"></div>

</div>


<!-- ADD PRODUCT -->
<div id="adminAddProductSection"
class="admin-section hidden">

<div class="admin-card">

<h2>➕ Tambah Produk</h2>

<br>

<label>Nama Produk</label>
<input id="newProductName" placeholder="Contoh: Premium VIP">

<label>Harga</label>
<input id="newProductPrice" type="number" placeholder="50000">

<label>Stok</label>
<input id="newProductStock" type="number" placeholder="10">

<label>URL Gambar Produk</label>
<input id="newProductImage" placeholder="https://...">

<button class="btn green full"
onclick="addProduct()">

➕ Tambahkan Produk

</button>

</div>

</div>


<!-- BANNERS -->
<div id="adminBannerSection"
class="admin-section hidden">

<h2>🖼️ Kelola Banner</h2>

<br>

<div class="admin-card">

<h3>➕ Tambah Banner</h3>

<label>Judul</label>
<input id="newBannerTitle" placeholder="Promo Spesial">

<label>Deskripsi</label>
<input id="newBannerDesc" placeholder="Diskon produk hari ini">

<label>URL Gambar Banner</label>
<input id="newBannerImage" placeholder="https://...">

<button class="btn green full"
onclick="addBanner()">

Tambah Banner

</button>

</div>

<br>

<div id="adminBannerGrid" class="grid"></div>

</div>


<!-- QRIS -->
<div id="adminQrisSection"
class="admin-section hidden">

<div class="admin-card">

<h2>💳 Pengaturan QRIS</h2>

<br>

<img
id="adminQrisPreview"
class="qris"
src=""
alt="QRIS Preview">

<label>URL Gambar QRIS</label>

<input
id="qrisInput"
placeholder="https://...">

<button
class="btn green full"
onclick="saveQris()">

💾 Simpan QRIS

</button>

</div>

</div>

</div>

</section>


<!-- MODAL -->
<div id="modal" class="modal hidden">

<div class="modal-box">

<h2>🎉 Transaksi Dibuat</h2>

<p id="modalText"></p>

<button class="btn" onclick="closeModal()">
OK
</button>

</div>

</div>


<script>

/* ================================
   DATABASE
================================ */

let users =
JSON.parse(localStorage.getItem("payx_users")) || [];

let transactions =
JSON.parse(localStorage.getItem("payx_transactions")) || [];

let products =
JSON.parse(localStorage.getItem("payx_products")) || [

{
id:1,
name:"Premium Basic",
price:10000,
stock:20,
image:"https://images.unsplash.com/photo-1511512578047-dfb367046420?w=900"
},

{
id:2,
name:"Premium Pro",
price:25000,
stock:15,
image:"https://images.unsplash.com/photo-1542751371-adc38448a05e?w=900"
},

{
id:3,
name:"Premium VIP",
price:50000,
stock:8,
image:"https://images.unsplash.com/photo-1493711662062-fa541adb3fc8?w=900"
}

];

let banners =
JSON.parse(localStorage.getItem("payx_banners")) || [

{
id:1,
title:"Selamat Datang di PayX",
desc:"Payment cepat menggunakan QRIS.",
image:"https://images.unsplash.com/photo-1556742049-0cfed4f6a45d?w=1400"
},

{
id:2,
title:"Promo Produk",
desc:"Dapatkan produk favorit kamu sekarang.",
image:"https://images.unsplash.com/photo-1556740749-887f6717d7e4?w=1400"
}

];

let qris =
localStorage.getItem("payx_qris") ||
"https://upload.wikimedia.org/wikipedia/commons/d/d0/QR_code_Wikipedia.svg";

let currentUser =
localStorage.getItem("payx_currentUser");

let selectedProduct=null;

const ADMIN_USER="admin";
const ADMIN_PASS="admin123";

const ADMIN_WHATSAPP="6283129373923";


/* ================================
   SAVE
================================ */

function saveAll(){

localStorage.setItem(
"payx_users",
JSON.stringify(users)
);

localStorage.setItem(
"payx_transactions",
JSON.stringify(transactions)
);

localStorage.setItem(
"payx_products",
JSON.stringify(products)
);

localStorage.setItem(
"payx_banners",
JSON.stringify(banners)
);

localStorage.setItem(
"payx_qris",
qris
);

}


/* ================================
   PAGE
================================ */

function hideAll(){

document
.querySelectorAll("body > section")
.forEach(x=>x.classList.add("hidden"));

}

function showLogin(){

hideAll();

document
.getElementById("loginPage")
.classList.remove("hidden");

}

function showRegister(){

hideAll();

document
.getElementById("registerPage")
.classList.remove("hidden");

}

function showAdminLogin(){

hideAll();

document
.getElementById("adminLoginPage")
.classList.remove("hidden");

}


/* ================================
   REGISTER
================================ */

function register(){

let username=
document.getElementById("regUser").value.trim();

let password=
document.getElementById("regPass").value;

if(!username||!password){

alert("Lengkapi data!");

return;

}

if(users.some(u=>u.username===username)){

alert("Username sudah digunakan!");

return;

}

users.push({
username,
password
});

saveAll();

alert("Pendaftaran berhasil!");

showLogin();

}


/* ================================
   LOGIN
================================ */

function login(){

let username=
document.getElementById("loginUser").value;

let password=
document.getElementById("loginPass").value;

let user=
users.find(
u=>u.username===username&&u.password===password
);

if(!user){

alert("Login gagal!");

return;

}

currentUser=username;

localStorage.setItem(
"payx_currentUser",
username
);

showStore();

}


/* ================================
   ADMIN LOGIN
================================ */

function adminLogin(){

let u=
document.getElementById("adminUser").value;

let p=
document.getElementById("adminPass").value;

if(u===ADMIN_USER&&p===ADMIN_PASS){

hideAll();

document
.getElementById("adminPage")
.classList.remove("hidden");

adminTab("dashboard");

}else{

alert("Login admin salah!");

}

}


/* ================================
   BUYER STORE
================================ */

function showStore(){

hideAll();

document
.getElementById("storePage")
.classList.remove("hidden");

renderProducts();
renderBanners();

}


/* ================================
   PRODUCTS BUYER
================================ */

function renderProducts(){

let grid=
document.getElementById("productGrid");

grid.innerHTML="";

products.forEach(p=>{

let sold=p.stock<=0;

grid.innerHTML+=`

<div class="card">

<img
class="product-image"
src="${p.image}"
onerror="this.src='https://via.placeholder.com/800x500/111625/ffffff?text=Product">

<div class="product-content">

<h3>${p.name}</h3>

<div class="price">
Rp ${format(p.price)}
</div>

<div class="stock ${sold?"empty":""}">
${sold?"❌ Stok Habis":"📦 Stok: "+p.stock}
</div>

<button
class="btn"
onclick="buyProduct(${p.id})"
${sold?"disabled":""}>

${sold?"Stok Habis":"Beli Sekarang"}

</button>

</div>
</div>

`;

});

}


/* ================================
   BANNER BUYER
================================ */

let bannerIndex=0;

function renderBanners(){

let track=
document.getElementById("bannerTrack");

let dots=
document.getElementById("bannerDots");

track.innerHTML="";
dots.innerHTML="";

banners.forEach((b,i)=>{

track.innerHTML+=`

<div
class="banner"
style="background-image:url('${b.image}')">

<div class="banner-content">

<h2>${b.title}</h2>

<p>${b.desc}</p>

</div>

</div>

`;

dots.innerHTML+=`

<div
class="dot ${i===0?"active":""}">
</div>

`;

});

bannerIndex=0;

if(banners.length>1){

setInterval(()=>{

bannerIndex++;

if(bannerIndex>=banners.length)
bannerIndex=0;

track.style.transform=
`translateX(-${bannerIndex*100}%)`;

document
.querySelectorAll(".dot")
.forEach((d,i)=>
d.classList.toggle(
"active",
i===bannerIndex
));

},4000);

}

}


/* ================================
   BUY
================================ */

function buyProduct(id){

selectedProduct=
products.find(p=>p.id===id);

if(!selectedProduct)return;

if(selectedProduct.stock<=0){

alert("Stok habis!");

return;

}

hideAll();

document
.getElementById("paymentPage")
.classList.remove("hidden");

document
.getElementById("paymentProduct")
innerText=
selectedProduct.name;

document
.getElementById("paymentTotal")
innerText=
"Rp "+format(selectedProduct.price);

document
.getElementById("qrisImage")
src=qris;

}


/* ================================
   PAYMENT
================================ */

function confirmPayment(){

if(!selectedProduct)return;

let id=
"PX"+Date.now();

transactions.push({

id:id,

user:currentUser,

product:selectedProduct.name,

price:selectedProduct.price,

status:"Pending",

date:new Date().toLocaleString("id-ID")

});

saveAll();

let message=

`Halo Admin PayX 👋

Saya sudah melakukan pembayaran.

🧾 ID Transaksi:
${id}

👤 Username:
${currentUser}

📦 Produk:
${selectedProduct.name}

💰 Total:
Rp ${format(selectedProduct.price)}

Mohon dicek dan di-ACC pembayaran saya.`;

window.open(
"https://wa.me/"+
ADMIN_WHATSAPP+
"?text="+
encodeURIComponent(message),
"_blank"
);

document
.getElementById("modalText")
.innerHTML=
`ID Transaksi: <b>${id}</b><br><br>
Status: <b>Pending</b><br><br>
WhatsApp Admin sudah dibuka.`;

document
.getElementById("modal")
.classList
.remove("hidden");

}


/* ================================
   TRANSACTIONS BUYER
================================ */

function showTransactions(){

hideAll();

document
.getElementById("transactionPage")
.classList
.remove("hidden");

let list=
document.getElementById("transactionList");

let data=
transactions.filter(
t=>t.user===currentUser
);

list.innerHTML="";

if(!data.length){

list.innerHTML=`
<tr>
<td colspan="5" style="text-align:center">
Belum ada transaksi.
</td>
</tr>`;

return;

}

data.slice().reverse().forEach(t=>{

let cls=
t.status==="Success"
?"success":
t.status==="Rejected"
?"rejected":"";

list.innerHTML+=`

<tr>

<td>${t.id}</td>
<td>${t.product}</td>
<td>Rp ${format(t.price)}</td>
<td>${t.date}</td>

<td>
<span class="status ${cls}">
${t.status}
</span>
</td>

</tr>

`;

});

}


/* ================================
   ADMIN TAB
================================ */

function adminTab(tab){

let sections=[
"adminDashboard",
"adminTransactionsSection",
"adminProductsSection",
"adminAddProductSection",
"adminBannerSection",
"adminQrisSection"
];

sections.forEach(id=>
document.getElementById(id)
.classList.add("hidden")
);

if(tab==="dashboard"){

document
.getElementById("adminDashboard")
.classList.remove("hidden");

renderStats();

}

if(tab==="transactions"){

document
.getElementById("adminTransactionsSection")
.classList.remove("hidden");

renderAdminTransactions();

}

if(tab==="products"){

document
.getElementById("adminProductsSection")
.classList.remove("hidden");

renderAdminProducts();

}

if(tab==="addproduct"){

document
.getElementById("adminAddProductSection")
.classList.remove("hidden");

}

if(tab==="banners"){

document
.getElementById("adminBannerSection")
.classList.remove("hidden");

renderAdminBanners();

}

if(tab==="qris"){

document
.getElementById("adminQrisSection")
.classList.remove("hidden");

document.getElementById("qrisInput").value=qris;

document.getElementById("adminQrisPreview").src=qris;

}

}


/* ================================
   ADMIN STATS
================================ */

function renderStats(){

document.getElementById("statTransactions")
.innerText=transactions.length;

document.getElementById("statPending")
.innerText=
transactions.filter(t=>t.status==="Pending").length;

document.getElementById("statSuccess")
.innerText=
transactions.filter(t=>t.status==="Success").length;

document.getElementById("statProducts")
.innerText=products.length;

let total=
transactions
.filter(t=>t.status==="Success")
.reduce((a,b)=>a+Number(b.price),0);

document.getElementById("statNominal")
.innerText="Rp "+format(total);

}


/* ================================
   ADMIN TRANSACTIONS
================================ */

function renderAdminTransactions(){

let list=
document.getElementById("adminTransactions");

list.innerHTML="";

transactions.slice().reverse().forEach(t=>{

let index=
transactions.findIndex(
x=>x.id===t.id
);

let cls=
t.status==="Success"
?"success":
t.status==="Rejected"
?"rejected":"";

let action=
t.status==="Pending"
?

`<button
class="btn green"
onclick="approve(${index})">
ACC
</button>

<button
class="btn red"
onclick="reject(${index})">
Tolak
</button>`

:"✓";

list.innerHTML+=`

<tr>

<td>${t.id}</td>
<td>${t.user}</td>
<td>${t.product}</td>
<td>Rp ${format(t.price)}</td>
<td>${t.date}</td>

<td>
<span class="status ${cls}">
${t.status}
</span>
</td>

<td>${action}</td>

</tr>

`;

});

}


/* ================================
   ACC
================================ */

function approve(index){

let t=transactions[index];

if(!t||t.status!=="Pending")return;

let product=
products.find(
p=>p.name===t.product
);

if(product){

if(product.stock<=0){

alert("Stok produk habis!");

return;

}

product.stock--;

}

t.status="Success";

saveAll();

alert("Pembayaran di-ACC!");

renderAdminTransactions();

}


/* ================================
   REJECT
================================ */

function reject(index){

if(!transactions[index])return;

transactions[index].status="Rejected";

saveAll();

alert("Pembayaran ditolak.");

renderAdminTransactions();

}


/* ================================
   ADMIN PRODUCTS
================================ */

function renderAdminProducts(){

let grid=
document.getElementById("adminProductGrid");

grid.innerHTML="";

products.forEach(p=>{

grid.innerHTML+=`

<div class="admin-card">

<img src="${p.image}">

<label>Nama Produk</label>

<input
id="pname${p.id}"
value="${p.name}">

<label>Harga</label>

<input
id="pprice${p.id}"
type="number"
value="${p.price}">

<label>Stok</label>

<input
id="pstock${p.id}"
type="number"
value="${p.stock}">

<label>URL Gambar</label>

<input
id="pimage${p.id}"
value="${p.image}">

<button
class="btn green full"
onclick="saveProduct(${p.id})">

💾 Simpan

</button>

<button
class="btn red full"
onclick="deleteProduct(${p.id})">

🗑️ Hapus Produk

</button>

</div>

`;

});

}


/* ================================
   SAVE PRODUCT
================================ */

function saveProduct(id){

let p=
products.find(x=>x.id===id);

if(!p)return;

p.name=
document.getElementById("pname"+id).value;

p.price=
Number(
document.getElementById("pprice"+id).value
);

p.stock=
Number(
document.getElementById("pstock"+id).value
);

p.image=
document.getElementById("pimage"+id).value;

saveAll();

alert("Produk diperbarui!");

renderAdminProducts();

}


/* ================================
   ADD PRODUCT
================================ */

function addProduct(){

let name=
document.getElementById("newProductName").value.trim();

let price=
Number(
document.getElementById("newProductPrice").value
);

let stock=
Number(
document.getElementById("newProductStock").value
);

let image=
document.getElementById("newProductImage").value.trim();

if(!name||price<0||stock<0){

alert("Lengkapi data produk!");

return;

}

products.push({

id:Date.now(),

name:name,

price:price,

stock:stock,

image:image||
"https://via.placeholder.com/800x500/111625/ffffff?text=Product"

});

saveAll();

document.getElementById("newProductName").value="";
document.getElementById("newProductPrice").value="";
document.getElementById("newProductStock").value="";
document.getElementById("newProductImage").value="";

alert("Produk berhasil ditambahkan!");

adminTab("products");

}


/* ================================
   DELETE PRODUCT
================================ */

function deleteProduct(id){

if(!confirm("Hapus produk ini?"))return;

products=
products.filter(p=>p.id!==id);

saveAll();

renderAdminProducts();

}


/* ================================
   ADMIN BANNER
================================ */

function renderAdminBanners(){

let grid=
document.getElementById("adminBannerGrid");

grid.innerHTML="";

banners.forEach(b=>{

grid.innerHTML+=`

<div class="admin-card">

<img src="${b.image}">

<label>Judul</label>

<input
id="btitle${b.id}"
value="${b.title}">

<label>Deskripsi</label>

<input
id="bdesc${b.id}"
value="${b.desc}">

<label>URL Gambar</label>

<input
id="bimage${b.id}"
value="${b.image}">

<button
class="btn green full"
onclick="saveBanner(${b.id})">

💾 Simpan Banner

</button>

<button
class="btn red full"
onclick="deleteBanner(${b.id})">

🗑️ Hapus Banner

</button>

</div>

`;

});

}


/* ================================
   ADD BANNER
================================ */

function addBanner(){

let title=
document.getElementById("newBannerTitle").value.trim();

let desc=
document.getElementById("newBannerDesc").value.trim();

let image=
document.getElementById("newBannerImage").value.trim();

if(!title||!image){

alert("Judul dan gambar wajib diisi!");

return;

}

banners.push({

id:Date.now(),

title:title,

desc:desc,

image:image

});

saveAll();

document.getElementById("newBannerTitle").value="";
document.getElementById("newBannerDesc").value="";
document.getElementById("newBannerImage").value="";

alert("Banner berhasil ditambahkan!");

renderAdminBanners();

}


/* ================================
   SAVE BANNER
================================ */

function saveBanner(id){

let b=
banners.find(x=>x.id===id);

if(!b)return;

b.title=
document.getElementById("btitle"+id).value;

b.desc=
document.getElementById("bdesc"+id).value;

b.image=
document.getElementById("bimage"+id).value;

saveAll();

alert("Banner diperbarui!");

renderAdminBanners();

}


/* ================================
   DELETE BANNER
================================ */

function deleteBanner(id){

if(!confirm("Hapus banner?"))return;

banners=
banners.filter(b=>b.id!==id);

saveAll();

renderAdminBanners();

}


/* ================================
   QRIS
================================ */

function saveQris(){

let url=
document
.getElementById("qrisInput")
.value.trim();

if(!url){

alert("URL QRIS tidak boleh kosong!");

return;

}

qris=url;

saveAll();

document
.getElementById("adminQrisPreview")
.src=qris;

alert("QRIS berhasil diperbarui!");

}


/* ================================
   CLOSE MODAL
================================ */

function closeModal(){

document
.getElementById("modal")
.classList
.add("hidden");

showTransactions();

}


/* ================================
   LOGOUT
================================ */

function logout(){

localStorage.removeItem(
"payx_currentUser"
);

currentUser=null;

showLogin();

}

function adminLogout(){

showLogin();

}


/* ================================
   FORMAT
================================ */

function format(n){

return Number(n)
.toLocaleString("id-ID");

}


/* ================================
   START
================================ */

if(currentUser){

showStore();

}else{

showLogin();

}

</script>

</body>
</html>
