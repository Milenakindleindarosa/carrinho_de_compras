<script setup>

import { ref, computed } from "vue";

const carrinho = 
{
  itens: 
  [
    {
      id: 1,
      nome: 'Combo Bubbaloo Morango',
    }
  ]
}

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
  
</template>

<style src="./assets/reset.css">
</style>

<style scoped>

</style>
