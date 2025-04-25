<script setup>

import { ref, computed } from "vue";

</script>



<template>

  <header>
    <div>
      <img src="https://res.cloudinary.com/beleza-na-web/image/upload/f_svg,fl_progressive,q_auto:eco/v1/blz/assets-store/0.0.505/images/store/47/logo.svg" alt="Logo-oBoticário">
      <div>
        <form action="">

          <p>
            <textarea name="pesquisa" id="pesquisar">Pesquisar</textarea>
            <input type="submit" value="">
          </p>
          
        </form>
      </div>
    </div>
  </header>

  <main>

    <section class="sugestao">

     <h2 class="sugestaoProduto">Sugestão de produto</h2>

      <ul>

        <li class="nome">Combo Cuide-se Bem Feira Cuidados Faciais: Gel de Limpeza Tangerina 150g + Hidratante Cremoso Banana 80g + Máscara Facial Noturna Melancia 50g</li>

        <li class="descricao">Com Cuide-se Bem Feira, a feira é diferente, está em toda parte, vai com você aonde você for, no dia e na hora que você quiser! O Combo Cuide-se Bem Feira Cuidados Faciais proporciona uma mistura de frutas tropicais para um skincare com diferentes fragrâncias, texturas e novas maneiras de se amar.</li>

      </ul>

        <ul class="precoImagem">

          <li class="preco">R$111,90<br>ou 3x de R$37,30</li>

          <li><img src="/images/sugestao.png" alt=""></li>

        </ul>

    </section>

  </main>
  
</template>

<style src="./assets/reset.css"></style>

<style scoped>

main section h2.sugestaoProduto{

background-color: rgb(209, 186, 255);
padding: 15px;
margin: 5vw 82vw 0 4vw;
font-size: 1.5rem;
text-align: center;

}

main section ul li.nome{

font-size: xx-large;
margin: 3vw 9vw 3vw 2vw;

}

</style>