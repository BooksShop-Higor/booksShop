<script setup>
import { RouterLink } from 'vue-router'
</script>

<template>
  <RouterLink to="/"></RouterLink>

  <main>
    <section class="banner">
      <h1>Carrinho</h1>
      <ul>
        <li>
          <h2>Título</h2>
        </li>
        <li>
          <h2>Qantidade</h2>
        </li>
        <li>
          <h2>Subtotal</h2>
        </li>
      </ul>
    </section>

    <section class="compra">
      <ul>
        <li v-for="lancamento in lancamentos" :key="lancamento.id">
          <img :src="lancamento.imagem" alt="">
          <h2>{{ lancamento.titulo }}</h2>
          <p>{{ lancamento.autor }}</p>
          <p class="bold">R${{ lancamento.preco }} <a href=""><span class="mdi mdi-heart-outline"
                style="color: #27AE60;"></span></a></p>
          <div>
            <button @click="incrementar(lancamento.id)">+</button>
            <p>{{ lancamento.quantidade }}</p>
            <button @click="decrementar">-</button>
            <p>{{ lancamento.precoTotal }}</p>
          </div>
        </li>
      </ul>

    </section>
  </main>
</template>

<style scoped></style>
