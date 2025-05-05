<script setup>
    import { ref } from "vue";

    const lancamentos1 = ref([
      {
        imagem: '../src/assets/books/cfi_vol2.png',
        titulo: 'Chsin of Iron: Volume 2',
        autor: 'Cassandra Clare',
        preco: '23.24'

      },
      {
        imagem: '../src/assets/books/cft.png',
        titulo: 'Chain of Thorns',
        autor: 'Cassandra Clare',
        preco: '23.24'

      },
      {
        imagem: '../src/assets/books/cofa.png',
        titulo: 'City of Fallen Angels',
        autor: 'Cassandra Clare',
        preco: '13.94'

      },
      {
        imagem: '../src/assets/books/nonaTheNinth.png',
        titulo: 'Nona The Ninth',
        autor: 'Cassandra Clare',
        preco: '16.84'
      },
      {
        imagem: '../src/assets/books/harlemS.png',
        titulo: 'Harlem Shuffle',
        autor: 'Colson Whitehead',
        preco: '26.92'

      },
      {
        imagem: '../src/assets/books/two.png',
        titulo: 'Two Old Women',
        autor: 'Velma Wallis',
        preco: '13.95'
      },
      {
        imagem: '../src/assets/books/carrie.png',
        titulo: 'Carrie Soto Is Back',
        autor: 'Taylor Jenkins Reid',
        preco: '26.04'

      },
      {
        imagem: '../src/assets/books/bookLovers.png',
        titulo: 'Book Lovers',
        autor: 'Emily Henry',
        preco: '15.81'
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
        <p>*within the stock limit</p>
      </li>
    </ul>
    </section>

    <section class="holder">
      <img src="../assets/caminhão.png" alt=""> <img src="../assets/line 2.png" alt="">
      <img src="../assets/estrela.png" alt="">  <img src="../assets/line 2.png" alt="">
      <img src="../assets/livros.png" alt="">
    </section>

    <section class="lancamentos">
      <h3>Lançamentos</h3>

      <ul>
        <li v-for="lancamento in lancamentos1" :key="lancamento.id">
        <img :src="lancamento.imagem" alt="">
        <h2>{{ lancamento.titulo }}</h2>
        <p>{{ lancamento.autor }}</p>
        <p class="bold">R${{ lancamento.preco }}</p>
        <button>Comprar</button>

        </li>
    </ul>

    </section>

  </main>


</template>

<style scoped>
  .banner ul {
    display: flex;
    padding: 2% 5%;
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
    text-align: end;
  }

  .banner {
    border-bottom: 1px solid #27AE60;
  }

  /* Formatação holder */

  .holder {
    display: flex;
    justify-content: space-between;
    padding: 5% 10%;
    border-bottom: solid #27AE60 1px;
  }

  /* for,atacao lançamentos */

  .lancamentos {
    padding: 4%;
  }

  .lancamentos h3 {
    font-weight: bold;
    font-size: 240%;
    margin-bottom: 3%;
  }

  .lancamentos ul {
    display: flex;
    flex-wrap: wrap ;
    justify-content: center;
  }

  .lancamentos li {
    margin-right: 5%;
    margin-bottom: 3%;
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
  }
</style>
