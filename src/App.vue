<script setup>
import { RouterLink } from 'vue-router'

</script>

<template>
  <header>
    <div id="logo">
      <p>IFbooks</p>
      <p><span>Apreço a<br>
        leitura</span></p>
    </div>
    <div id="search">
      <input type="text" placeholder="Pesquisar" id="input-search">
    <img id="image-search" src="../src/assets/lupa.png" alt="Lupa">
    </div>
    <nav>
      <ul id="header-page-links">
        <li><a href="#">Termos</a></li>
        <li><a href="#">Equipe</a></li>
        <li><a href="#">Envio</a></li>
        <li><a href="#">Devoluções</a></li>
      </ul>
    </nav>

      <RouterLink class="image-links" to="/carrinho"> <span class="mdi mdi-cart" style="color: #27AE60; font-size: 1.5rem;"></span></RouterLink>
      <p class="divisao-links">|</p>
      <a class="image-links" href="#"><span class="mdi mdi-heart" style="color: #27AE60; font-size: 1.5rem;"></span></a>
      <p class="divisao-links">|</p>
      <a class="image-links" href="#"><span class="mdi mdi-account" style="color: #27AE60; font-size: 1.5rem;"></span></a>
  </header>


  <router-view></router-view>

  <footer>
    <div class="footer">
      <div class="redesSo">
        <ul>
          <h3>IFbooks</h3>
          <li>
            <a href="https://www.facebook.com/"><span class="fa-brands fa-square-facebook" style="color: white;"></span></a>
            <a href="https://www.instagram.com/"><span class="fa-brands fa-square-instagram" style="color: white;"></span></a>
            <a href="https://x.com/"><span class="fa-brands fa-square-x-twitter" style="color: white;"></span></a>
          </li>
        </ul>
      </div>
      <div class="contato">
        <h2>Contatos</h2>
        <ul>
          <li>
            <span class="mdi mdi-phone"></span>
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
    <p class="direitos">© Alguns direitos reservados. IFbooks 2025.</p>
  </footer>
</template>

<style scoped>

  /* formatação header  */

 header{
    padding: 1vw 10vw;
    background-color: white;
    display: flex;
    justify-content: space-between;
    border-bottom: 2px #27AE60 solid;
  }
  header #logo{
    display: flex;
  }
  header #logo p{
    font-size: 1.5rem;
    color: #231F2D;
    padding-right: 0.5vw;
    margin-top: 0.5vw;
  }
  header #logo p span{
    font-size: 0.8rem;
    color: #27AE60;
    padding-left: 0.5vw;
    padding-right: 0;
    display: inline-block;
    border-left: 2px #27AE60 solid;
    margin-top: 0;
    margin-right: 2vw;
  }

  header #search {
    display: flex;
    align-items: center;
    text-align: center;
  }
  header #input-search{
    font-family: inherit;
    font-size: inherit;
    background-color: #F1F1F1;
    border: none;
    color: #B8B8B8;
    padding: 0.7rem 1rem;
    border-radius: 2px;
    width: 30em;
    transition: all ease-in-out .5s;
    margin-right: -2vw;
  }
  header #search img{
    width: 20px;
  }
  header #input-search:focus {
    outline: 1px solid #B8B8B8;
  }
  header #image-search:hover {
    cursor: pointer;
  }
  header #header-page-links {
    list-style: none;
    display: flex;
  }
  header #header-page-links li{
    margin: 1vw;
  }
  header #header-page-links li a{
    color: #7B7881;
    text-decoration: none;
    transition: all ease-in-out .5s;
  }
  header #header-page-links li a:hover{
    text-decoration: underline;
  }
  header .image-links {
    padding-top: 0.5vw;
  }
  header .divisao-links{
    font-size: 30px;
    color: #27AE60;
  }

  /* formatação footer */


  footer {
    background-color: #27AE60;
    color: white;
    padding: 3% 0;
  }

  div.footer {
    display: flex;
    justify-content: space-between;
    margin: 0 10%;
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
    font-size: 240%;
    margin-right: 4%;
  }

  div.contato  span {
    font-size: 100%;
  }

  div.contato li {
    align-items: center;
    justify-content: space-between;
    margin: 5% 0;
  }

  footer img {
    margin-top: 30%;
  }

  p.direitos {
    text-align: center;
    margin-top: 3%;
    border-top: solid #F1F1F1 2px;
    padding-top: 2% ;
  }

</style>
