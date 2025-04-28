<script setup>
</script>

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
            <span class="mdi mdi-cart" style="color: #27AE60;"></span>
          </RouterLink>
          <img src="../src/assets/Line 1.png" class="separation">
          <span class="mdi mdi-heart-outline" style="color: #27AE60;"></span>
          <img src="../src/assets/Line 1.png" class="separation">
          <span class="mdi mdi-account-outline" style="color: #27AE60;"></span>
        </div>
      </li>
    </ul>
  </header>

  <router-view></router-view>

  <footer>
    <div class="footer">
      <div>
        <ul>
          <h3>IFbooks</h3>
          <li>
            <span class="fa-brands fa-square-facebook"></span>
            <span class="fa-brands fa-square-instagram"></span>
            <span class="fa-brands fa-square-x-twitter"></span>
          </li>
        </ul>
      </div>
      <div class="contato">
        <h2>Contatos</h2>
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

  /* formatação header  */

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
  }

  div.icons {
    margin-left: 100%;
  }

  div.icons span {
    font-size: 180%;
    margin: 0 10%;
  }

  div.icons img {
    margin: 0 10%;
  }

  /* formatação footer */


  footer {
    background-color: #27AE60;
    color: white;
    padding: 5% 8%;
  }

  div.footer {
    display: flex;
    justify-content: space-between;
  }

  div.footer p {
    font-size: 110%;
  }

  div.footer h2 {
    font-weight: bold;
    font-size: 130%;
  }
  div.footer h3 {
    font-size: 140%;
  }

  div.contato ul li {
    display: flex;


  }
  div.contato ul {
    justify-content: space-between;
  }

  div.footer span {
    font-size: 260%;
    margin: 0 2%;
  }
</style>
