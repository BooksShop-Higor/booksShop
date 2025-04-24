<script setup></script>

<template>
  <header>
    <ul>
      <li class="pesquisa">
        <h3>IFbooks</h3>
        <img src="../src/assets/Line 1.png" alt="">
        <p>
          Apreço a
          leitura
        </p>
        <div>
          <img src="../src/assets/lupa.png" alt="" />
          <input type="text" placeholder="Pesquisar" />
        </div>
      </li>
      <li>
        <nav>
          <a href="">Termos</a>
          <a href="">Equipe</a>
          <a href="">Envio</a>
          <a href="">Devoluções</a>
        </nav>
        <div class="icons">
          <RouterLink to="/carrinho">
            <span class="fa-solid fa-cart-shopping" style="color: #63e6be"></span>
          </RouterLink>
          <span class="fa-solid fa-heart" style="color: #63e6be"></span>
          <span class="fa-solid fa-user" style="color: #63e6be"></span>
        </div>
      </li>
    </ul>
  </header>

  <router-view></router-view>

  <footer>
    <div class="footer">
      <div>
        <ul>
          <p>IFbooks</p>
          <li>
            <span class="fa-brands fa-square-facebook"></span>
            <span class="fa-brands fa-square-instagram"></span>
            <span class="fa-brands fa-square-x-twitter"></span>
          </li>
        </ul>
      </div>
      <div>
        <h3>Contatos</h3>
        <ul>
          <li>
            <span class="fa-solid fa-phone"></span>
            <p>+55 47 40045263</p>
          </li>
          <li>
            <span class="fa-solid fa-clock"></span>
            <p>8h às 23h - Seg a Sex</p>
          </li>
          <li>
            <span class="fa-solid fa-envelope"></span>
            <p>contato@ifbooks.com</p>
          </li>
        </ul>
        <img src="../src/assets/ways to pay.png" alt="" />
      </div>
    </div>
    <p>© Alguns direitos reservados. IFbooks 2025.</p>
  </footer>
</template>

<style scoped>
  header {
    margin: 2vw 8vw;
  }
  nav {
    display: flex;
    margin-left: 30%;
  }

  header ul {
    display: flex;
    justify-content: center;
    justify-content: flex-start;
  }

  header li {
    display: flex;

  }
  header h3 {
    font-size: 160%;
    text-align: center;
  }
  header p {
    color: #27ae5f7e;
    line-height: 120%;
  }

  header img {
    margin: 0 1% 0 2%;
    font-size: 45%;
  }

  header li div {
    display: flex;
  }

  input {
  background-color: #F1F1F1;
  margin-left: 6%;
  width: 30vw;
  height: 120%;
  color: #B8B8B8;
  border: none;
  padding: 0 0 0 2%;
  }

  header ul li:first-child div img {
  margin-left: 28%;
  margin-top: 0.7%;
  position: absolute;
  }

  nav a {
    margin-right: 30%;
    font-size: 130%;
    color: #7B7881;
    justify-content: center;
  }

  div.icons {
    margin-left: 120%;
  }

  div.icons span {
    font-size: 150%;
  }
</style>