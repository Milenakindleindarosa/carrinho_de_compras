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

        <li class="nome">
          Combo Cuide-se Bem Feira Cuidados Faciais: Gel de Limpeza Tangerina 150g + Hidratante Cremoso Banana 80g + Máscara Facial Noturna Melancia 50g</li>

        <li class="descricao"><p>Com Cuide-se Bem Feira, a feira é diferente, está em toda parte, vai com você aonde você for, no dia e na hora que você quiser!<br> O Combo Cuide-se Bem Feira Cuidados Faciais proporciona uma mistura de frutas tropicais para um skincare com diferentes fragrâncias, texturas e novas maneiras de se amar.</p></li>

        </ul>

        <div>

             <p class="preco">R$111,90</p>

             <p class="imagem"><img src="/images/sugestao.png" alt=""></p>

        </div>

    </section>

  </main>
  
<section class="footer">

<footer>

<ul>

<li class="titulo">Contato</li>

<li>Seg. à sex., 8h às 20h - Sáb., 9h às 18h</li>

<li>41 3406-8393</li>

</ul>

</footer>

</section>

</template>

<style src="./assets/reset.css"></style>

<style scoped>

main section h2.sugestaoProduto{

background-color: rgb(209, 186, 255);
padding: 15px;
margin: 5vw 82vw 0 4vw;
font-size: 1.6rem;
text-align: center;

}

main section ul li.nome{

font-size: xx-large;
margin: 3vw 9vw 3vw 2vw;

}

main section.sugestao div p.preco{

font-size: 3rem;
margin: 23vw 0 16vw 13vw;
border: 5px solid rgb(209, 186, 255);
background-color: rgb(209, 186, 255);
padding: 2px;

}

main section.sugestao div p{

margin: 0 15vw 0 0;

}

main section div{

justify-content: space-between;
width: 93%;
display: flex;

}

main section ul li.descricao{

font-size: 1.2vw;
color: rgb(80, 80, 80);
margin: 0 0 0.7vw 1vw;

}

main section.sugestao div p.imagem img{

  margin: 5vw 0 12vw 20vw;

}

section.footer footer{

background-color: rgb(209, 186, 255);;

}

</style>