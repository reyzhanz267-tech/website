<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>BANG JAYY | Modern Art Sablon</title>
    <!-- Font Awesome 6 -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <!-- Google Fonts: Inter + Space Grotesk (modern) -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700;14..32,800&family=Space+Grotesk:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background-color: #ffffff;
            color: #111111;
            scroll-behavior: smooth;
        }

        /* Modern art geometric background */
        .bg-art {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -2;
            background: linear-gradient(125deg, #faf9f7 0%, #f0ede8 100%);
        }
        .bg-art::before {
            content: '';
            position: absolute;
            top: 10%;
            right: -5%;
            width: 400px;
            height: 400px;
            background: radial-gradient(circle, rgba(230, 30, 50, 0.04) 0%, transparent 70%);
            border-radius: 50%;
        }
        .bg-art::after {
            content: '';
            position: absolute;
            bottom: 5%;
            left: -5%;
            width: 500px;
            height: 500px;
            background: radial-gradient(circle, rgba(230, 30, 50, 0.03) 0%, transparent 70%);
            border-radius: 50%;
        }

        /* geometric shapes */
        .shape-1, .shape-2 {
            position: fixed;
            z-index: -1;
            opacity: 0.3;
        }
        .shape-1 {
            top: 20%;
            left: -50px;
            width: 300px;
            height: 300px;
            border: 2px solid #e11e32;
            transform: rotate(45deg);
        }
        .shape-2 {
            bottom: 15%;
            right: -30px;
            width: 250px;
            height: 250px;
            background: #e11e32;
            clip-path: polygon(25% 0%, 100% 0%, 75% 100%, 0% 100%);
            opacity: 0.05;
        }

        /* navbar modern */
        .navbar {
            background: rgba(255,255,255,0.92);
            backdrop-filter: blur(12px);
            position: sticky;
            top: 0;
            z-index: 100;
            padding: 1.2rem 2.5rem;
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 1rem;
            border-bottom: 1px solid rgba(0,0,0,0.05);
        }

        .logo h1 {
            font-size: 1.6rem;
            font-weight: 700;
            font-family: 'Space Grotesk', sans-serif;
            letter-spacing: -0.02em;
            background: linear-gradient(135deg, #111111, #e11e32);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
        }
        .logo span {
            font-size: 0.75rem;
            font-weight: 400;
            color: #666;
            letter-spacing: 0.3px;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            align-items: center;
            flex-wrap: wrap;
        }
        .nav-links a {
            text-decoration: none;
            font-weight: 500;
            color: #1a1a1a;
            transition: 0.2s;
            cursor: pointer;
            font-size: 0.9rem;
        }
        .nav-links a:hover { color: #e11e32; }
        .admin-login-btn {
            background: #111;
            color: white;
            padding: 0.4rem 1.2rem;
            border-radius: 40px;
            font-size: 0.8rem;
            font-weight: 500;
            transition: 0.2s;
        }
        .admin-login-btn:hover { background: #e11e32; color: white; }
        .admin-logged-badge {
            background: #e11e32;
            color: white;
            padding: 0.3rem 1rem;
            border-radius: 40px;
            font-size: 0.8rem;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        .cart-icon {
            position: relative;
            font-size: 1.3rem;
            cursor: pointer;
            color: #1a1a1a;
        }
        .cart-count {
            position: absolute;
            top: -8px;
            right: -10px;
            background: #e11e32;
            color: white;
            font-size: 0.65rem;
            font-weight: bold;
            border-radius: 50%;
            padding: 0.15rem 0.45rem;
            min-width: 18px;
            text-align: center;
        }

        /* floating social minimal */
        .float-social {
            position: fixed;
            bottom: 30px;
            right: 25px;
            z-index: 999;
            display: flex;
            flex-direction: column;
            gap: 12px;
        }
        .float-btn {
            width: 48px;
            height: 48px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.4rem;
            transition: 0.2s;
            text-decoration: none;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
        }
        .btn-wa { background: #25D366; }
        .btn-tiktok { background: #000; }
        .float-btn:hover { transform: scale(1.05); opacity: 0.9; }

        /* hero modern */
        .hero {
            padding: 4rem 2rem;
            text-align: center;
            max-width: 900px;
            margin: 0 auto;
        }
        .hero h2 {
            font-size: 3.5rem;
            font-weight: 800;
            font-family: 'Space Grotesk', sans-serif;
            letter-spacing: -0.03em;
            line-height: 1.2;
            background: linear-gradient(125deg, #111 30%, #e11e32 70%);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
        }
        .hero p {
            font-size: 1.1rem;
            color: #444;
            margin: 1.2rem auto;
            max-width: 550px;
        }
        .hero-address {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: #f0f0f0;
            padding: 0.5rem 1.2rem;
            border-radius: 50px;
            font-size: 0.85rem;
            margin: 1rem 0;
            color: #333;
        }
        .social-icons-hero {
            display: flex;
            gap: 1rem;
            justify-content: center;
            margin: 1.5rem 0;
        }
        .hero-social-btn {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: transparent;
            padding: 0.5rem 1.2rem;
            border-radius: 40px;
            text-decoration: none;
            font-weight: 500;
            font-size: 0.85rem;
            border: 1px solid #ccc;
            transition: 0.2s;
            color: #111;
        }
        .hero-social-btn:hover { border-color: #e11e32; background: #e11e32; color: white; }
        .btn-order {
            background: #111;
            color: white;
            border: none;
            padding: 0.8rem 2rem;
            border-radius: 40px;
            font-weight: 600;
            cursor: pointer;
            margin-top: 1rem;
            transition: 0.2s;
        }
        .btn-order:hover { background: #e11e32; transform: scale(1.02); }

        .container {
            max-width: 1300px;
            margin: 0 auto;
            padding: 1rem 2rem 3rem;
        }
        .section-title {
            font-size: 1.8rem;
            font-weight: 700;
            font-family: 'Space Grotesk', sans-serif;
            margin: 2rem 0 1.5rem;
            letter-spacing: -0.02em;
            border-left: 4px solid #e11e32;
            padding-left: 1rem;
        }
        .filter-wrap {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
            gap: 1rem;
            margin-bottom: 2rem;
        }
        .ukuran-filter {
            display: flex;
            gap: 0.6rem;
            flex-wrap: wrap;
        }
        .filter-btn {
            background: #f4f4f4;
            border: none;
            padding: 0.5rem 1.2rem;
            border-radius: 40px;
            font-weight: 500;
            cursor: pointer;
            transition: 0.2s;
            font-size: 0.85rem;
        }
        .filter-btn.active {
            background: #111;
            color: white;
        }
        .motif-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(290px, 1fr));
            gap: 2rem;
            margin-top: 1rem;
        }
        .card {
            background: white;
            border-radius: 1.5rem;
            overflow: hidden;
            transition: 0.25s ease;
            border: 1px solid #eee;
            box-shadow: 0 4px 12px rgba(0,0,0,0.02);
        }
        .card:hover {
            transform: translateY(-6px);
            box-shadow: 0 20px 30px rgba(0,0,0,0.05);
            border-color: #e11e32;
        }
        .card-img {
            background: #faf9f7;
            height: 240px;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
        }
        .product-image {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        .image-placeholder {
            font-size: 3.5rem;
            color: #aaa;
        }
        .card-info {
            padding: 1.2rem;
        }
        .motif-name {
            font-size: 1.2rem;
            font-weight: 700;
            letter-spacing: -0.3px;
        }
        .price {
            font-size: 1.2rem;
            font-weight: 700;
            color: #e11e32;
            margin: 0.4rem 0;
        }
        .ukuran-options {
            display: flex;
            gap: 0.5rem;
            margin: 0.6rem 0;
            flex-wrap: wrap;
        }
        .size-badge {
            background: #f0f0f0;
            padding: 0.25rem 0.7rem;
            border-radius: 30px;
            font-size: 0.7rem;
            font-weight: 500;
        }
        .btn-add {
            background: #111;
            color: white;
            width: 100%;
            padding: 0.7rem;
            border: none;
            border-radius: 50px;
            font-weight: 600;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            cursor: pointer;
            transition: 0.2s;
            margin-top: 0.7rem;
        }
        .btn-add:hover { background: #e11e32; }

        /* admin modals */
        .login-modal, .admin-modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.7);
            backdrop-filter: blur(4px);
            z-index: 2000;
            justify-content: center;
            align-items: center;
        }
        .login-modal.active, .admin-modal.active { display: flex; }
        .login-panel, .admin-panel {
            background: white;
            width: 90%;
            max-width: 450px;
            border-radius: 28px;
            padding: 2rem;
            text-align: center;
        }
        .admin-panel { max-width: 800px; text-align: left; max-height: 85vh; overflow-y: auto; }
        .admin-header { display: flex; justify-content: space-between; align-items: center; border-bottom: 2px solid #e11e32; padding-bottom: 0.8rem; margin-bottom: 1.2rem; }
        .admin-product-item { border: 1px solid #ddd; border-radius: 1rem; padding: 1rem; margin-bottom: 1rem; display: flex; gap: 1rem; flex-wrap: wrap; align-items: center; }
        .upload-btn, .save-product-btn { background: #111; color: white; padding: 0.4rem 1rem; border-radius: 30px; border: none; cursor: pointer; margin: 0.2rem; }
        .save-product-btn { background: #10b981; }
        .close-admin, .close-login { background: #e11e32; color: white; border: none; padding: 0.4rem 1rem; border-radius: 30px; cursor: pointer; margin-top: 1rem; }

        .cart-sidebar {
            position: fixed;
            top: 0;
            right: -400px;
            width: 380px;
            height: 100%;
            background: white;
            box-shadow: -5px 0 20px rgba(0,0,0,0.1);
            z-index: 1000;
            transition: 0.3s ease;
            display: flex;
            flex-direction: column;
            padding: 1.5rem;
        }
        .cart-sidebar.open { right: 0; }
        .cart-header { font-size: 1.3rem; font-weight: 700; padding-bottom: 1rem; border-bottom: 1px solid #eee; }
        .cart-items { flex: 1; overflow-y: auto; margin: 1rem 0; }
        .cart-item { display: flex; justify-content: space-between; margin-bottom: 1rem; padding-bottom: 0.8rem; border-bottom: 1px solid #f0f0f0; }
        .cart-total { font-weight: 800; font-size: 1.2rem; border-top: 2px dashed #e11e32; padding-top: 1rem; margin: 1rem 0; }
        .checkout-btn { background: #111; color: white; border: none; padding: 0.8rem; border-radius: 50px; width: 100%; cursor: pointer; font-weight: 600; }
        .overlay { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.3); z-index: 999; display: none; }
        .overlay.active { display: block; }
        footer { text-align: center; padding: 2rem; color: #777; font-size: 0.8rem; border-top: 1px solid #eee; margin-top: 2rem; }
        .toast-msg { position: fixed; bottom: 20px; left: 50%; transform: translateX(-50%); background: #111; color: white; padding: 0.5rem 1.2rem; border-radius: 40px; font-size: 0.8rem; z-index: 1100; opacity: 0; transition: 0.2s; pointer-events: none; }
        @media (max-width: 680px) { .navbar { padding: 1rem; } .hero h2 { font-size: 2.2rem; } .cart-sidebar { width: 100%; right: -100%; } }
    </style>
</head>
<body>
<div class="bg-art"></div>
<div class="shape-1"></div>
<div class="shape-2"></div>

<div class="navbar">
    <div class="logo">
        <h1>BANG JAYY</h1>
        <span>modern art · sablon studio</span>
    </div>
    <div class="nav-links">
        <a id="homeBtn">Beranda</a>
        <a id="scrollToProdukLink">Koleksi</a>
        <a id="contactBtn">Studio</a>
        <div id="adminNavBtn"></div>
        <div class="cart-icon" id="cartIcon">
            <i class="fas fa-bag-shopping"></i>
            <span class="cart-count" id="cartCount">0</span>
        </div>
    </div>
</div>

<div class="float-social">
    <a href="#" target="_blank" class="float-btn btn-wa" id="floatWaBtn"><i class="fab fa-whatsapp"></i></a>
    <a href="#" target="_blank" class="float-btn btn-tiktok" id="floatTiktokBtn"><i class="fab fa-tiktok"></i></a>
</div>

<section class="hero">
    <h2>sablon kontemporer<br>untuk gaya masa kini</h2>
    <p>Koleksi eksklusif dengan sentuhan modern art. Ukuran lengkap, kualitas premium.</p>
    <div class="hero-address">
        <i class="fas fa-location-dot"></i> Jl. Besar Serdang Bedagai, Sei Rejo, Sergai
    </div>
    <div class="social-icons-hero">
        <a href="#" target="_blank" class="hero-social-btn" id="heroWaBtn"><i class="fab fa-whatsapp"></i> WhatsApp</a>
        <a href="#" target="_blank" class="hero-social-btn" id="heroTiktokBtn"><i class="fab fa-tiktok"></i> TikTok</a>
    </div>
    <button class="btn-order" id="scrollToProdukBtn">eksplorasi koleksi →</button>
</section>

<div class="container" id="produk">
    <div class="filter-wrap">
        <div class="ukuran-filter" id="sizeFilterContainer">
            <button class="filter-btn active" data-size="all">semua ukuran</button>
            <button class="filter-btn" data-size="S">S</button><button class="filter-btn" data-size="M">M</button>
            <button class="filter-btn" data-size="L">L</button><button class="filter-btn" data-size="XL">XL</button>
            <button class="filter-btn" data-size="XXL">XXL</button><button class="filter-btn" data-size="3XL">3XL</button>
        </div>
        <div style="font-size:0.75rem; background:#f4f4f4; padding:5px 12px; border-radius:30px;"><i class="fas fa-palette"></i> filter berdasarkan ukuran</div>
    </div>
    <h3 class="section-title">koleksi terbaru</h3>
    <div class="motif-grid" id="motifGrid"></div>
</div>

<!-- login admin -->
<div id="loginModal" class="login-modal">
    <div class="login-panel">
        <i class="fas fa-lock" style="font-size:2rem; color:#e11e32;"></i>
        <h3 style="margin:1rem 0;">akses admin</h3>
        <input type="password" id="adminPassword" placeholder="password" style="width:100%; padding:0.8rem; border:1px solid #ddd; border-radius:40px; margin-bottom:1rem;">
        <button id="loginSubmitBtn" style="background:#111; color:white; border:none; padding:0.7rem; width:100%; border-radius:40px; font-weight:600;">masuk</button>
        <div id="loginError" style="color:#e11e32; margin-top:0.5rem; font-size:0.8rem;"></div>
        <button class="close-login" id="closeLoginBtn" style="margin-top:1rem;">tutup</button>
    </div>
</div>

<!-- admin panel -->
<div id="adminModal" class="admin-modal">
    <div class="admin-panel">
        <div class="admin-header"><h3 style="font-weight:700;">edit produk · bang jayy studio</h3><button class="close-admin" id="closeAdminBtn">✕ tutup</button></div>
        <div id="adminProductList"></div>
    </div>
</div>

<div class="overlay" id="overlay"></div>
<div class="cart-sidebar" id="cartSidebar">
    <div class="cart-header">keranjang belanja</div>
    <div class="cart-items" id="cartItemsList"><div style="color:#aaa;">keranjang kosong</div></div>
    <div class="cart-total" id="cartTotal">total: Rp0</div>
    <button class="checkout-btn" id="checkoutBtn">checkout →</button>
    <button class="close-cart" id="closeCartBtn" style="margin-top:1rem; background:none; border:none; text-decoration:underline; cursor:pointer; color:#777;">tutup</button>
</div>
<div id="toastMsg" class="toast-msg"></div>

<script>
    // config
    const ADMIN_PASSWORD = "bangjayy123";
    const WHATSAPP_NUMBER = "62895405445092";
    const WHATSAPP_MESSAGE = "Halo Bang Jayy, saya mau pesan kaus modern art";
    const TIKTOK_URL = "https://www.tiktok.com/@bgjayy_27?_r=1&_t=ZS-96d0hrfo5zR";
    
    let isAdminLoggedIn = false;
    let motifs = [
        { id: 1, name: "abstract flux", icon: "◉", price: 125000, availableSizes: ["S","M","L","XL","XXL","3XL"], imageData: null },
        { id: 2, name: "mono chrome", icon: "⬤", price: 119000, availableSizes: ["M","L","XL","XXL"], imageData: null },
        { id: 3, name: "neon stroke", icon: "◈", price: 135000, availableSizes: ["S","M","L","XL"], imageData: null },
        { id: 4, name: "geometric noise", icon: "▣", price: 129000, availableSizes: ["L","XL","XXL","3XL"], imageData: null },
        { id: 5, name: "minimal wave", icon: "〰️", price: 115000, availableSizes: ["S","M","L","XL","XXL","3XL"], imageData: null },
        { id: 6, name: "texture play", icon: "▓", price: 139000, availableSizes: ["M","L","XL","XXL"], imageData: null },
        { id: 7, name: "blur edge", icon: "◌", price: 122000, availableSizes: ["S","M","L","XL"], imageData: null },
        { id: 8, name: "bold contrast", icon: "◆", price: 145000, availableSizes: ["L","XL","XXL","3XL"], imageData: null }
    ];
    
    let cart = [];
    let activeSizeFilter = "all";
    
    function saveAllData() { localStorage.setItem('bangjayy_modern_products', JSON.stringify(motifs.map(m => ({ id: m.id, name: m.name, price: m.price, imageData: m.imageData })))); }
    function loadAllData() { let stored = localStorage.getItem('bangjayy_modern_products'); if(stored){ try{ let arr = JSON.parse(stored); arr.forEach(sp => { let m = motifs.find(mot=>mot.id===sp.id); if(m){ if(sp.name) m.name = sp.name; if(sp.price) m.price = sp.price; if(sp.imageData) m.imageData = sp.imageData; } }); }catch(e){} } }
    
    function updateSocial() { let wa = `https://wa.me/${WHATSAPP_NUMBER}?text=${encodeURIComponent(WHATSAPP_MESSAGE)}`; document.querySelectorAll('#floatWaBtn, #heroWaBtn').forEach(btn => btn.href=wa); document.querySelectorAll('#floatTiktokBtn, #heroTiktokBtn').forEach(btn => btn.href=TIKTOK_URL); }
    
    // admin session
    function checkAdmin() { if(localStorage.getItem('bangjayy_admin_session')==='true') isAdminLoggedIn=true; updateAdminUI(); }
    function saveAdmin() { localStorage.setItem('bangjayy_admin_session','true'); isAdminLoggedIn=true; updateAdminUI(); }
    function logoutAdmin() { localStorage.removeItem('bangjayy_admin_session'); isAdminLoggedIn=false; updateAdminUI(); closeAdminModal(); showToast("admin logout"); }
    function updateAdminUI(){
        let container = document.getElementById('adminNavBtn'); if(!container) return;
        if(isAdminLoggedIn){
            container.innerHTML = `<div class="admin-logged-badge"><i class="fas fa-user"></i> admin <button class="logout-btn" id="logoutAdminBtn" style="background:none; border:none; color:white; cursor:pointer;">✕</button></div><a id="openAdminPanelBtn" style="margin-left:8px; background:#e11e32; padding:0.3rem 1rem; border-radius:40px; font-size:0.8rem; cursor:pointer;">✎ edit produk</a>`;
            document.getElementById('logoutAdminBtn')?.addEventListener('click', logoutAdmin);
            document.getElementById('openAdminPanelBtn')?.addEventListener('click', ()=>{ renderAdminPanel(); openAdminModal(); });
        } else {
            container.innerHTML = `<a id="showLoginBtn" class="admin-login-btn"><i class="fas fa-lock"></i> admin</a>`;
            document.getElementById('showLoginBtn')?.addEventListener('click', ()=> openLoginModal());
        }
    }
    
    const loginModal = document.getElementById('loginModal');
    function openLoginModal(){ loginModal.classList.add('active'); document.getElementById('adminPassword').value=''; document.getElementById('loginError').innerText=''; }
    function closeLoginModal(){ loginModal.classList.remove('active'); }
    document.getElementById('loginSubmitBtn')?.addEventListener('click', ()=>{ if(document.getElementById('adminPassword').value === ADMIN_PASSWORD){ saveAdmin(); closeLoginModal(); showToast("selamat datang admin"); renderAdminPanel(); openAdminModal(); } else { document.getElementById('loginError').innerText='password salah'; } });
    document.getElementById('closeLoginBtn')?.addEventListener('click', closeLoginModal);
    window.addEventListener('click', (e)=>{ if(e.target===loginModal) closeLoginModal(); });
    
    const adminModal = document.getElementById('adminModal');
    function openAdminModal(){ if(!isAdminLoggedIn){ showToast("login sebagai admin dulu"); openLoginModal(); return; } adminModal.classList.add('active'); }
    function closeAdminModal(){ adminModal.classList.remove('active'); }
    document.getElementById('closeAdminBtn')?.addEventListener('click', closeAdminModal);
    window.addEventListener('click', (e)=>{ if(e.target===adminModal) closeAdminModal(); });
    
    function renderAdminPanel(){
        let container = document.getElementById('adminProductList'); if(!container) return;
        container.innerHTML = motifs.map(m => `<div class="admin-product-item"><div style="width:70px;height:70px;background:#f4f4f4;border-radius:12px;display:flex;align-items:center;justify-content:center;">${m.imageData ? `<img src="${m.imageData}" style="width:70px;height:70px;object-fit:cover;border-radius:12px;">` : `<span style="font-size:2rem;">${m.icon}</span>`}</div><div style="flex:1"><input type="text" class="prod-name" data-id="${m.id}" value="${m.name.replace(/"/g,'&quot;')}" style="width:100%; padding:0.5rem; margin-bottom:0.4rem; border:1px solid #ddd; border-radius:12px;"><input type="number" class="prod-price" data-id="${m.id}" value="${m.price}" style="width:120px; padding:0.5rem; border:1px solid #ddd; border-radius:12px;"></div><div><input type="file" accept="image/png" class="img-upload" data-id="${m.id}" style="display:none;"><button class="upload-btn" data-id="${m.id}"><i class="fas fa-image"></i> png</button><button class="save-product-btn" data-id="${m.id}" style="margin-left:5px;"><i class="fas fa-save"></i> simpan</button></div></div>`).join('');
        document.querySelectorAll('.upload-btn').forEach(btn => btn.addEventListener('click', (e)=>{ let id = btn.dataset.id; document.querySelector(`.img-upload[data-id='${id}']`).click(); }));
        document.querySelectorAll('.img-upload').forEach(inp => inp.addEventListener('change', (e)=>{ let id = parseInt(inp.dataset.id); let file = e.target.files[0]; if(file && file.type==='image/png'){ if(file.size>2*1024*1024){ showToast("max 2mb"); return; } let rd = new FileReader(); rd.onload = ev => { let m = motifs.find(mot=>mot.id===id); if(m){ m.imageData = ev.target.result; saveAllData(); renderMotifs(); renderAdminPanel(); showToast("gambar diperbarui"); } }; rd.readAsDataURL(file); } else { showToast("pilih file PNG"); } inp.value=''; }));
        document.querySelectorAll('.save-product-btn').forEach(btn => btn.addEventListener('click', ()=>{ let id = parseInt(btn.dataset.id); let newName = document.querySelector(`.prod-name[data-id='${id}']`).value; let newPrice = parseInt(document.querySelector(`.prod-price[data-id='${id}']`).value); let m = motifs.find(mot=>mot.id===id); if(m){ if(newName) m.name = newName; if(!isNaN(newPrice) && newPrice>0) m.price = newPrice; saveAllData(); renderMotifs(); renderAdminPanel(); showToast("produk tersimpan"); } }));
    }
    
    function renderMotifs(){
        let grid = document.getElementById('motifGrid'); if(!grid) return;
        let filtered = activeSizeFilter === 'all' ? motifs : motifs.filter(m => m.availableSizes.includes(activeSizeFilter));
        if(filtered.length===0){ grid.innerHTML = `<div style="grid-column:1/-1; text-align:center; padding:3rem;">tidak ada produk untuk ukuran ini</div>`; return; }
        grid.innerHTML = filtered.map(m => `<div class="card"><div class="card-img">${m.imageData ? `<img class="product-image" src="${m.imageData}">` : `<div class="image-placeholder"><i class="fas fa-palette" style="font-size:3rem; color:#ccc;"></i><div style="margin-top:8px;">${m.icon}</div></div>`}</div><div class="card-info"><div class="motif-name">${m.name}</div><div class="price">Rp ${m.price.toLocaleString('id-ID')}</div><div class="ukuran-options">${m.availableSizes.map(sz=>`<span class="size-badge">${sz}</span>`).join('')}</div><select id="sizeDrop-${m.id}" style="width:100%; padding:8px; border-radius:30px; border:1px solid #ddd; margin:8px 0;">${m.availableSizes.map(sz=>`<option value="${sz}">ukuran ${sz}</option>`).join('')}</select><button class="btn-add" data-id="${m.id}" data-name="${m.name}" data-price="${m.price}" data-icon="${m.icon}"><i class="fas fa-bag-shopping"></i> tambah ke keranjang</button></div></div>`).join('');
        document.querySelectorAll('.btn-add').forEach(btn => btn.addEventListener('click', addToCart));
    }
    
    function addToCart(e){
        let btn = e.currentTarget;
        let id = parseInt(btn.dataset.id), name = btn.dataset.name, price = parseInt(btn.dataset.price), icon = btn.dataset.icon;
        let size = document.getElementById(`sizeDrop-${id}`).value;
        let exist = cart.find(i => i.id === id && i.size === size);
        if(exist) exist.quantity++; else cart.push({ id, motifName: name, size, price, icon, quantity: 1 });
        updateCart(); showToast(`✓ ${name} (${size}) ditambahkan`);
    }
    
    function updateCart(){
        let container = document.getElementById('cartItemsList'); let totalSpan = document.getElementById('cartTotal');
        if(cart.length===0){ container.innerHTML = '<div style="color:#aaa;">keranjang kosong</div>'; totalSpan.innerText = 'total: Rp0'; updateCount(); return; }
        let total=0, html='';
        cart.forEach((item,idx)=>{ let sub = item.price*item.quantity; total+=sub; html+=`<div class="cart-item"><div><strong>${item.icon} ${item.motifName}</strong><br>${item.size} x${item.quantity}<br>@${item.price.toLocaleString()}</div><div>Rp${sub.toLocaleString()}<br><button class="cart-qty-minus" data-idx="${idx}">-</button> <button class="cart-qty-plus" data-idx="${idx}">+</button> <button class="cart-del" data-idx="${idx}"><i class="fas fa-trash-alt"></i></button></div></div>`; });
        container.innerHTML = html; totalSpan.innerText = `total: Rp${total.toLocaleString('id-ID')}`;
        document.querySelectorAll('.cart-qty-plus').forEach(btn=>btn.addEventListener('click',()=>{ let i=parseInt(btn.dataset.idx); if(cart[i]){ cart[i].quantity++; updateCart(); } }));
        document.querySelectorAll('.cart-qty-minus').forEach(btn=>btn.addEventListener('click',()=>{ let i=parseInt(btn.dataset.idx); if(cart[i]){ if(cart[i].quantity>1) cart[i].quantity--; else cart.splice(i,1); updateCart(); } }));
        document.querySelectorAll('.cart-del').forEach(btn=>btn.addEventListener('click',()=>{ let i=parseInt(btn.dataset.idx); if(cart[i]){ cart.splice(i,1); updateCart(); } }));
        updateCount();
    }
    function updateCount(){ document.getElementById('cartCount').innerText = cart.reduce((s,i)=>s+i.quantity,0); }
    function showToast(msg){ let t=document.getElementById('toastMsg'); t.innerText=msg; t.style.opacity='1'; setTimeout(()=>t.style.opacity='0',1800); }
    
    // cart sidebar
    const cartIcon = document.getElementById('cartIcon'), cartSidebar = document.getElementById('cartSidebar'), overlay = document.getElementById('overlay'), closeCartBtn = document.getElementById('closeCartBtn');
    function openCart(){ cartSidebar.classList.add('open'); overlay.classList.add('active'); }
    function closeCart(){ cartSidebar.classList.remove('open'); overlay.classList.remove('active'); }
    cartIcon.addEventListener('click', openCart); closeCartBtn.addEventListener('click', closeCart); overlay.addEventListener('click', closeCart);
    document.getElementById('checkoutBtn').addEventListener('click',()=>{ if(cart.length===0){ showToast("keranjang kosong"); return; } let sum = "BANG JAYY MODERN ART\n\n"; cart.forEach(i=>sum+=`${i.motifName} (${i.size}) x${i.quantity} = Rp${(i.price*i.quantity).toLocaleString()}\n`); sum+=`\ntotal: Rp${cart.reduce((s,i)=>s+(i.price*i.quantity),0).toLocaleString()}\n\nTerima kasih! Admin akan menghubungi Anda.`; alert(sum); });
    
    // filters
    document.querySelectorAll('.filter-btn').forEach(btn=>btn.addEventListener('click',()=>{ document.querySelectorAll('.filter-btn').forEach(b=>b.classList.remove('active')); btn.classList.add('active'); activeSizeFilter = btn.dataset.size; renderMotifs(); }));
    document.getElementById('scrollToProdukBtn')?.addEventListener('click',()=>document.getElementById('produk').scrollIntoView({behavior:'smooth'}));
    document.getElementById('scrollToProdukLink')?.addEventListener('click',()=>document.getElementById('produk').scrollIntoView({behavior:'smooth'}));
    document.getElementById('homeBtn')?.addEventListener('click',()=>window.scrollTo({top:0,behavior:'smooth'}));
    document.getElementById('contactBtn')?.addEventListener('click',()=>alert("📍 BANG JAYY STUDIO\n\nJl. Besar Serdang Bedagai, Sei Rejo, Sergai\n📞 WA: 0895-4054-45092\n📱 TikTok: @bgjayy_27\n\nJam buka: 09.00 - 21.00\nModern art sablon studio."));
    
    loadAllData(); renderMotifs(); updateCart(); updateSocial(); checkAdmin();
</script>
<footer>
    <p>© 2025 BANG JAYY — modern art sablon studio</p>
    <p style="margin-top:6px;">Jl. Besar Serdang Bedagai, Sei Rejo, Sergai | desain eksklusif · ukuran lengkap</p>
</footer>
</body>
</html>
