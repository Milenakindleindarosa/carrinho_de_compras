<script setup>

import { ref, computed } from "vue";

</script>



<template>
  <header>
    <div >

      <img src="https://res.cloudinary.com/beleza-na-web/image/upload/f_svg,fl_progressive,q_auto:eco/v1/blz/assets-store/0.0.505/images/store/47/logo.svg" alt="Logo-oBoticário">

      <div>
        <form action="">

          <p>
            <input type="text" v-model="input" placeholder="Pesquisar..."/>
            <button>
              <span class="fa-solid fa-magnifying-glass" ></span>
            </button>
          </p> 

        </form>
      </div>

      <ul class="links">
        <li>
          <a href="">Termos</a>
        </li>
        <li>
          <a href="">Equipe</a>
        </li>
        <li>
          <a href="">Envio</a>
        </li>
        <li>
          <a href="">Devoluções</a>
        </li>
      </ul>

      <ul class="icones">
        <li @click="abrirCarrinho">
          <p>
            <span class="fa-solid fa-cart-shopping"></span>
          </p>
        </li>
        <li>
          <p>
            <span class="fa-solid fa-heart"></span>
          </p>
        </li>
        <li>
          <p>
            <span class="fa-solid fa-user"></span>
          </p>
        </li>
      </ul>

    </div>
  </header>

<footer>

<ul class="contato">

<li>Contato: 41 3406-8393</li>

<li>Seg. à sex., 8h às 20h - Sáb., 9h às 18h</li>

</ul>

<ul class="icones">

<li><i class="fa-brands fa-square-facebook"></i></li>

<li><i class="fa-brands fa-square-instagram"></i></li>

<li><i class="fa-brands fa-square-twitter"></i></li>

<li><i class="fa-brands fa-square-youtube"></i></li>

<li><i class="fa-brands fa-square-whatsapp"></i></li>

<li><i class="fa-solid fa-square-phone"></i></li>

</ul>

<ul class="cartoes">

<li><i class="fa-brands fa-cc-visa"></i></li>

<li><i class="fa-brands fa-cc-mastercard"></i></li>

<li><i class="fa-brands fa-pix"></i></li>

</ul>

</footer>

</template>

<style src="./assets/reset.css">
</style>

<style scoped>

</style>