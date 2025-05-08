<script setup>
  import {ref} from 'vue'

    const lancamentos = ref([
  {
    imagem: '../src/assets/books/cfi_vol2.png',
    titulo: 'Chsin of Iron: Volume 2',
    autor: 'Cassandra Clare',
    preco: '23.24',
    quantidade: 0,
    id: '0'

  },
  {
    imagem: '../src/assets/books/cft.png',
    titulo: 'Chain of Thorns',
    autor: 'Cassandra Clare',
    preco: '23.24',
    quantidade: 0,
    id: '1'


  },
  {
    imagem: '../src/assets/books/cofa.png',
    titulo: 'City of Fallen Angels',
    autor: 'Cassandra Clare',
    preco: '13.94',
    quantidade: 0,
    id: '2'

  },
  {
    imagem: '../src/assets/books/nonaTheNinth.png',
    titulo: 'Nona The Ninth',
    autor: 'Cassandra Clare',
    preco: '16.84',
    quantidade: 0,
    id: '3'

  },
  {
    imagem: '../src/assets/books/harlemS.png',
    titulo: 'Harlem Shuffle',
    autor: 'Colson Whitehead',
    preco: '26.92',
    quantidade: 0,
    id: '4'

  },
  {
    imagem: '../src/assets/books/two.png',
    titulo: 'Two Old Women',
    autor: 'Velma Wallis',
    preco: '13.95',
    quantidade: 0,
    id:'5'
  },
  {
    imagem: '../src/assets/books/carrie.png',
    titulo: 'Carrie Soto Is Back',
    autor: 'Taylor Jenkins Reid',
    preco: '26.04',
    quantidade: 0,
    id:'6'

  },
  {
    imagem: '../src/assets/books/bookLovers.png',
    titulo: 'Book Lovers',
    autor: 'Emily Henry',
    precoTotal: '15.81',
    preco: '15.81',
    quantidade: 0,
    id: '7'
  }
 ])

</script>

<template>

  <main>
    <section class="banner">
      <ul>
      <li>
        <button>Autor de Abril</button>
        <h1>Erick-Manuel Scimitt</h1>
        <p>Eric-Emmanuel Schmitt has been awarded more than 20 literary prizes and distinctions, and in 2001 he received the title of Chevalier des Arts et des Lettres. His books have been translated into over 40 languages.</p>
        <button class="acesso">Acessar Página do Livro</button>
      </li>
      <li>
        <img src="../assets/book.png" alt="">
      </li>
    </ul>
    </section>

    <section class="holder">
      <ul>
        <li>
          <span class="mdi mdi-truck" style="color: black;"></span>
          <h2>Frete grátis para SC</h2>
        </li>
        <li class="meio">
          <span class="mdi mdi-star" style="color: black;"></span>
          <h2>Livros Recomendados</h2>
        </li>
        <li>
          <span class="mdi mdi-book-open-page-variant" style="color: black;"></span>
          <h2>Mais vendidos</h2>
        </li>
      </ul>
    </section>

    <section class="lancamentos">
      <h3>Lançamentos</h3>

      <ul>
        <li v-for="lancamento in lancamentos" :key="lancamento.id">
        <img :src="lancamento.imagem" alt="">
        <h2>{{ lancamento.titulo }}</h2>
        <p>{{ lancamento.autor }}</p>
        <p class="bold">R${{ lancamento.preco }} <a href=""><span class="mdi mdi-heart-outline" style="color: #27AE60;"></span></a></p>
        <button><span class="mdi mdi-cart" style="color: white;"></span>Comprar</button>

        </li>
      </ul>

    </section>

  </main>


</template>

<style scoped>
  .banner ul {
    display: flex;
    padding: 2% 8%;
    align-items: center;
    justify-content: space-between;
  }

  .banner ul li button {
    background-color: white;
    color: #27AE60;
    border: 1px solid #27AE60;
    padding: 0.5%;
    border-radius: 5px;
    height: 40px;
    width: 10%;
  }

  .banner h1 {
    font-weight: bold;
    font-size: 320%;
    color: black;
    margin-top: 2%;
  }

  .banner p {
    font-size: 130%;
    padding-right: 40%;
  }

  .banner button.acesso {
    background-color: #27AE60;
    color: white;
    width: 20%;
    height: 50px;
    font-size: 110%;
    font-weight: bold;
    margin-top: 4%;
    border-radius: 1.5px;
  }

  .banner ul li:last-child p {
    margin-left: 10%;
  }

  .banner {
    border-bottom: 1px solid #27AE60;
  }

  /* Formatação holder */

  .holder {
    padding: 5%;
    border-bottom: solid #27AE60 1px;
  }
  .holder h2 {
    color: black;
    font-weight: bold;
  }

  .holder ul {
    display: flex;
    justify-content: center;
  }

  .holder li {
    display: flex;
    font-size: 100%;
    align-items: center;
  }

  .holder .meio {
    border-right: solid black 2px ;
    border-left: solid black 2px;
    padding: 0 10%;
  }

  .holder li:first-child {
    padding-right: 10%;
  }

  .holder li:last-child {
    padding-left: 10%;
  }

  .holder span {
    font-size: 300%;
  }

  /* formatacao lançamentos */

  .lancamentos {
    padding: 3%;
    color: black;
  }

  .lancamentos h3 {
    font-weight: bold;
    font-size: 240%;
    margin-bottom: 5%;
    margin-left: 9%;
  }

  .lancamentos ul {
    display: flex;
    flex-wrap: wrap ;
    justify-content: center;
  }

  .lancamentos li {
    margin-right: 5%;
    margin-bottom: 5%;
  }

  .lancamentos h2 {
    font-weight: bold;
  }

  .lancamentos p {
    margin-bottom: 3%;
  }

  .lancamentos .bold {
    font-weight: bold;
    font-size: 120%;
  }

  .lancamentos button {
    color: white;
    background-color: #27AE60;
    width: 100%;
    height: 8%;
    justify-content: space-between;
    font-size: 110%;
  }

  .lancamentos .bold a span {
    margin-left: 60%;
    font-size: 150%;
  }
</style>
