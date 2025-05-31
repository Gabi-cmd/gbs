<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>GbabySP - Fantasias Sofisticadas</title>
<style>
  /* Reset e fonte */
  * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; }
  body {
    background: #f9f7f1;
    color: #3b3a30;
  }
  header {
    background: linear-gradient(90deg, #bfa94b, #a68633);
    color: white;
    padding: 15px 30px;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  header .logo {
    font-weight: 900;
    font-size: 28px;
    letter-spacing: 2px;
    cursor: default;
  }
  header .logo span {
    font-size: 16px;
    vertical-align: super;
    font-weight: 600;
  }
  nav {
    display: flex;
    align-items: center;
    gap: 20px;
  }
  nav button {
    background: transparent;
    border: 2px solid white;
    color: white;
    padding: 8px 14px;
    border-radius: 20px;
    font-weight: 600;
    cursor: pointer;
    transition: background-color 0.3s;
  }
  nav button:hover {
    background-color: white;
    color: #a68633;
  }
  nav #cartBtn {
    position: relative;
  }
  nav #cartCount {
    position: absolute;
    top: -6px;
    right: -10px;
    background: #8c6c12;
    color: white;
    font-size: 12px;
    padding: 3px 7px;
    border-radius: 50%;
  }
  main {
    max-width: 1200px;
    margin: 30px auto;
    padding: 0 20px;
  }
  .product-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill,minmax(280px,1fr));
    gap: 30px;
  }
  .product {
    background: white;
    border-radius: 12px;
    box-shadow: 0 4px 8px rgb(191 169 75 / 0.2);
    padding: 15px;
    display: flex;
    flex-direction: column;
    align-items: center;
    transition: box-shadow 0.3s;
  }
  .product:hover {
    box-shadow: 0 8px 16px rgb(191 169 75 / 0.4);
  }
  .product img {
    max-width: 220px;
    border-radius: 10px;
    margin-bottom: 12px;
  }
  .product h3 {
    font-weight: 700;
    margin-bottom: 8px;
    text-align: center;
    min-height: 60px;
  }
  .product .price {
    font-size: 20px;
    font-weight: 700;
    color: #a68633;
    margin-bottom: 15px;
  }
  .product button {
    background: #bfa94b;
    border: none;
    padding: 10px 22px;
    font-weight: 700;
    color: white;
    border-radius: 25px;
    cursor: pointer;
    transition: background-color 0.3s;
  }
  .product button:hover {
    background-color: #a68633;
  }
  /* Carrinho */
  #cartModal {
    position: fixed;
    top: 60px;
    right: 20px;
    background: white;
    border: 2px solid #bfa94b;
    border-radius: 15px;
    padding: 20px;
    width: 320px;
    max-height: 400px;
    overflow-y: auto;
    box-shadow: 0 8px 16px rgb(191 169 75 / 0.5);
    display: none;
    z-index: 1000;
  }
  #cartModal h2 {
    color: #a68633;
    margin-bottom: 12px;
  }
  #cartModal ul {
    list-style: none;
  }
  #cartModal li {
    margin-bottom: 10px;
    border-bottom: 1px solid #eee;
    padding-bottom: 6px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  #cartModal li button {
    background: transparent;
    border: none;
    color: #a68633;
    font-weight: 700;
    cursor: pointer;
    font-size: 18px;
    line-height: 1;
  }
  #cartTotal {
    font-weight: 700;
    margin-top: 12px;
    text-align: right;
    font-size: 18px;
    color: #a68633;
  }
  #checkoutBtn {
    margin-top: 15px;
    width: 100%;
    padding: 10px 0;
    border: none;
    background: #a68633;
    color: white;
    font-weight: 700;
    border-radius: 25px;
    cursor: pointer;
    transition: background-color 0.3s;
  }
  #checkoutBtn:hover {
    background-color: #8c6c12;
  }
  /* Login */
  #loginSection {
    max-width: 320px;
    margin: 20px auto;
    background: white;
    padding: 25px 20px;
    border-radius: 15px;
    box-shadow: 0 6px 12px rgb(191 169 75 / 0.3);
  }
  #loginSection input {
    width: 100%;
    padding: 10px 12px;
    margin-bottom: 15px;
    border: 2px solid #bfa94b;
    border-radius: 10px;
    font-size: 16px;
  }
  #loginSection button {
    width: 100%;
    background: #bfa94b;
    border: none;
    padding: 12px 0;
    color: white;
    font-weight: 700;
    border-radius: 25px;
    cursor: pointer;
    transition: background-color 0.3s;
  }
  #loginSection button:hover {
    background-color: #a68633;
  }
  #loginMsg {
    margin-top: 10px;
    font-weight: 600;
    text-align: center;
  }
  /* Admin Panel */
  #adminSection {
    max-width: 900px;
    margin: 30px auto;
    background: white;
    border-radius: 15px;
    padding: 25px 20px;
    box-shadow: 0 6px 15px rgb(191 169 75 / 0.35);
  }
  #adminSection h2 {
    color: #a68633;
    margin-bottom: 20px;
    text-align: center;
  }
  #adminSection table {
    width: 100%;
    border-collapse: collapse;
  }
  #adminSection th, #adminSection td {
    border: 1px solid #bfa94b;
    padding: 10px 8px;
    text-align: center;
  }
  #adminSection th {
    background-color: #f1e9b0;
  }
  #adminSection input[type="text"],
  #adminSection input[type="number"] {
    width: 90%;
    padding: 5px;
    border: 1px solid #a68633;
    border-radius: 8px;
    font-size: 14px;
  }
  #adminSection button {
    background: #bfa94b;
    border: none;
    color: white;
    font-weight: 700;
    padding: 6px 14px;
    border-radius: 20px;
    cursor: pointer;
    transition: background-color 0.3s;
  }
  #adminSection button:hover {
    background-color: #a68633;
  }
  /* Botão sair admin */
  #logoutBtn {
    margin-top: 15px;
    background: #a42f2f;
  }
  /* Esconder elementos */
  .hidden {
    display: none;
  }
</style>
</head>
<body>

<header>
  <div class="logo">GBS<span>👑</span></div>
  <nav>
    <button id="loginBtn">Login</button>
    <button id="cartBtn">Carrinho <span id="cartCount">0</span></button>
  </nav>
</header>

<main>
  <section id="productSection">
    <h1 style="text-align:center; margin-bottom: 20px;">Fantasias Disponíveis</h1>
    <div class="product-grid" id="productGrid">
      <!-- Produtos serão gerados via JS -->
    </div>
  </section>

  <section id="loginSection" class="hidden">
    <h2>Login Administrativo</h2>
    <input type="text" id="username" placeholder="Usuário" />
    <input type="password" id="password" placeholder="Senha" />
    <button id="loginSubmit">Entrar</button>
    <div id="loginMsg"></div>
  </section>

  <section id="adminSection" class="hidden">
    <h2>Painel Admin</h2>
    <table id="adminTable">
      <thead>
        <tr>
          <th>ID</th><th>Nome</th><th>Preço (R$)</th><th>Estoque</th><th>Ações</th>
        </tr>
      </thead>
      <tbody>
        <!-- Produtos admin -->
      </tbody>
    </table>
    <button id="logoutBtn">Sair</button>
  </section>
</main>

<div id="cartModal" class="hidden">
  <h2>Carrinho de Compras</h2>
  <ul id="cartList"></ul>
  <div id="cartTotal">Total: R$ 0,00</div>
  <button id="checkoutBtn">Finalizar Compra</button>
</div>

<script>
  // Produtos exemplo
  const products = [
    {id:1, name:"Fada Dourada", price:129.90, stock:10, img:"https://i.imgur.com/7eQHn6D.jpg"},
    {id:2, name:"Pirata Chique", price:159.90, stock:5, img:"https://i.imgur.com/f2o9G3V.jpg"},
    {id:3, name:"Cavaleira Negra", price:189.90, stock:3, img:"https://i.imgur.com/Olnvw6K.jpg"},
    {id:4, name:"Maga Real", price:179.90, stock:7, img:"https://i.imgur.com/4jNwmud.jpg"},
  ];

  // Estado
  let cart = [];
  let adminLoggedIn = false;

  // DOM elements
  const productGrid = document.getElementById("productGrid");
  const cartBtn = document.getElementById("cartBtn");
  const cartCount = document.getElementById("cartCount");
  const cartModal = document.getElementById("cartModal");
  const cartList = document.getElementById("cartList");
  const cartTotal = document.getElementById("cartTotal");
  const checkoutBtn = document.getElementById("checkoutBtn");
  const loginBtn = document.getElementById("loginBtn");
  const loginSection = document.getElementById("loginSection");
  const adminSection = document.getElementById("adminSection");
  const loginSubmit = document.getElementById("loginSubmit");
  const loginMsg = document.getElementById("loginMsg");
  const logoutBtn = document.getElementById("logoutBtn");
  const adminTableBody = document.querySelector("#adminTable tbody");

  // Renderizar produtos na página principal
  function renderProducts() {
    productGrid.innerHTML = "";
    products.forEach(p => {
      const div = document.createElement("div");
      div.className = "product";
      div.innerHTML = `
        <img src="${p.img}" alt="${p.name}" />
        <h3>${p.name}</h3>
        <div class="price">R$ ${p.price.toFixed(2).replace(".", ",")}</div>
        <button ${p.stock === 0 ? "disabled" : ""} data-id="${p.id}">${p.stock === 0 ? "Esgotado" : "Comprar"}</button>
      `;
      productGrid.appendChild(div);
    });
  }

  // Atualizar contador do carrinho
  function updateCartCount() {
    const totalItems = cart.reduce((acc, item) => acc + item.qty, 0);
    cartCount.textContent = totalItems;
  }

  // Atualizar modal do carrinho
  function renderCart() {
    cartList.innerHTML = "";
    if(cart.length === 0){
      cartList.innerHTML = "<li>Seu carrinho está vazio.</li>";
      cartTotal.textContent = "Total: R$ 0,00";
      checkoutBtn.disabled = true;
      return;
    }
    checkoutBtn.disabled = false;
    let total = 0;
    cart.forEach(item => {
      const product = products.find(p => p.id === item.id);
      const li = document.createElement("li");
      li.innerHTML = `
        ${product.name} x ${item.qty} 
        <button data-id="${item.id}">&times;</button>
      `;
      cartList.appendChild(li);
      total += product.price * item.qty;
    });
    cartTotal.textContent = `Total: R$ ${total.toFixed(2).replace(".", ",")}`;
  }

  // Adicionar produto ao carrinho
  function addToCart(id) {
    const product = products.find(p => p.id === id);
    if(!product || product.stock === 0) return;
    const cartItem = cart.find(c => c.id === id);
    if(cartItem){
      if(cartItem.qty < product.stock){
        cartItem.qty++;
      } else {
        alert("Quantidade máxima em estoque atingida.");
      }
    } else {
      cart.push({id: id, qty: 1});
    }
    updateCartCount();
  }

  // Remover item do carrinho
  function removeFromCart(id) {
    cart = cart.filter(item => item.id !== id);
    updateCartCount();
  }

  // Eventos

  // Comprar (botões comprar)
  productGrid.addEventListener("click", e => {
    if(e.target.tagName === "BUTTON"){
      const id = parseInt(e.target.dataset.id);
      addToCart(id);
      alert("Produto adicionado ao carrinho!");
    }
  });

  // Abrir/fechar carrinho
  cartBtn.addEventListener("click", () => {
    if(cartModal.style.display === "block"){
      cartModal.style.display = "none";
      cartModal.classList.add("hidden");
    } else {
      renderCart();
      cartModal.style.display = "block";
      cartModal.classList.remove("hidden");
    }
  });

  // Remover do carrinho (clicar no X)
  cartList.addEventListener("click", e => {
    if(e.target.tagName === "BUTTON"){
      const id = parseInt(e.target.dataset.id);
      removeFromCart(id);
      renderCart();
    }
  });

  // Finalizar compra (simples alert)
  checkoutBtn.addEventListener("click", () => {
    if(!adminLoggedIn){
      alert("Você precisa estar logado para finalizar a compra.");
      return;
    }
    alert("Compra finalizada! Obrigada pela preferência.");
    cart = [];
    updateCartCount();
    cartModal.style.display = "none";
    cartModal.classList.add("hidden");
  });

  // Mostrar seção login
  loginBtn.addEventListener("click", () => {
    if(adminLoggedIn){
      alert("Você já está logado no painel admin.");
      return;
    }
    loginSection.classList.toggle("hidden");
  });

  // Login admin (simples)
  loginSubmit.addEventListener("click", () => {
    const user = document.getElementById("username").value.trim();
    const pass = document.getElementById("password").value.trim();
    if(user === "admin" && pass === "admin123"){
      adminLoggedIn = true;
      loginMsg.textContent = "Login bem-sucedido!";
      loginSection.classList.add("hidden");
      loginBtn.textContent = "Admin";
      renderAdminPanel();
      adminSection.classList.remove("hidden");
    } else {
      loginMsg.textContent = "Usuário ou senha incorretos.";
    }
  });

  // Render admin panel
  function renderAdminPanel(){
    adminTableBody.innerHTML = "";
    products.forEach(p => {
      const tr = document.createElement("tr");
      tr.innerHTML = `
        <td>${p.id}</td>
        <td><input type="text" value="${p.name}" data-id="${p.id}" class="edit-name" /></td>
        <td><input type="number" min="0" step="0.01" value="${p.price}" data-id="${p.id}" class="edit-price" /></td>
        <td><input type="number" min="0" value="${p.stock}" data-id="${p.id}" class="edit-stock" /></td>
        <td><button data-id="${p.id}" class="save-btn">Salvar</button></td>
      `;
      adminTableBody.appendChild(tr);
    });
  }

  // Salvar alterações admin
  adminTableBody.addEventListener("click", e => {
    if(e.target.classList.contains("save-btn")){
      const id = parseInt(e.target.dataset.id);
      const row = e.target.closest("tr");
      const newName = row.querySelector(".edit-name").value.trim();
      const newPrice = parseFloat(row.querySelector(".edit-price").value);
      const newStock = parseInt(row.querySelector(".edit-stock").value);
      if(newName === "" || isNaN(newPrice) || isNaN(newStock) || newPrice < 0 || newStock < 0){
        alert("Valores inválidos.");
        return;
      }
      const product = products.find(p => p.id === id);
      product.name = newName;
      product.price = newPrice;
      product.stock = newStock;
      alert("Produto atualizado.");
      renderProducts();
    }
  });

  // Logout admin
  logoutBtn.addEventListener("click", () => {
    adminLoggedIn = false;
    adminSection.classList.add("hidden");
    loginBtn.textContent = "Login";
    alert("Você saiu do painel admin.");
  });

  // Inicializar
  renderProducts();
  updateCartCount();
</script>

</body>
</html>
