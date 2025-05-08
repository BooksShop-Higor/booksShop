<script setup>
import {RouterLink} from 'vue-router'
import {ref } from "vue"

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

      }
    ])

const number = ref(23.24)

function encrementar() {
    number.value++
  }

  function decrementar() {
    number.value - number.value
  }
</script>

<template>
<RouterLink to="/"></RouterLink>

<main>
    <section class="banner">
      <h1>Carrinho</h1>
      <ul>
        <li><h2>Título</h2></li>
        <li><h2>Qantidade</h2></li>
        <li><h2>Subtotal</h2></li>
      </ul>
    </section>

    <section class="compra">
      <ul>
        <li v-for="lancamento in lancamentos1" :key="lancamento.id">
        <img :src="lancamento.imagem" alt="">
        <h2>{{ lancamento.titulo }}</h2>
        <p>{{ lancamento.autor }}</p>
        <p class="bold">R${{ lancamento.preco }} <a href=""><span class="mdi mdi-heart-outline" style="color: #27AE60;"></span></a></p>
        </li>
      </ul>
      <div>
        <button @click="encrementar">+</button>
        <p>{{ number }}</p>
        <button @click="decrementar">-</button>
      </div>
    </section>
  </main>
</template>

<style scoped>

</style>
