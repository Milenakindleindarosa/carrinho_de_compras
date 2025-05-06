<script setup>

import { ref, computed } from "vue";

function incrementar(compra, carrinho) 
{
  compra.quantidade++
  carrinho.totalCompra = 0
  for (let item of carrinho.itens) 
  {
    item.valorTotal = item.preco * item.quantidade;
    carrinho.totalCompra = totalCompra + item.valorTota;
  }
}

function decrementar(compra, carrinho)
{
  compra.quantidade--
  if (compra.quantidade === 0) 
  {
    itens.splice(index, 1)
  }
}

function adicionarCarrinho(produto, carrinho)
{
  let novoItem = ref 
    (
      [
        {
          id: 0,
          nome: '',
          resumo: '',
          preco: 0,
          img: '',
          quantidade: 1,
          valorTotal: 0,
        }
      ]
    )

  novoItem.id = produto.id;
  novoItem.nome = produto.nome;
  novoItem.resumo = produto.resumo;
  novoItem.preco = produto.preco;
  novoItem.img = produto.img;
  novoItem.valorTotal = produto.preco * produto.quantidade;

  for (let categoria of carrinhos.itens) 
  {
    categoria.valorTotal = categoria.quantidade * categoria.preco;
    if (categoria.id === produto.id)
    {
      categoria.quantidade++
      break;
    }
  }
  itens.push(novoItem)

  total();
}

function total()
{
  carrinho.totalCompra = 0
  for (let item of carrinho.itens) 
  {
    item.valorTotal = item.preco * item.quantidade
    carrinho.totalCompra = totalCompra + item.valorTotal
  }
}

const produtos = ref 
(
  [
    {
      id: 1,
      nome: 'Combo Bubbaloo Morango',
      resumo: 'Gloss 5 ml + Loção Hidratante Desodorante Corporal 200ml.',
      resenha: 'O Combo Bubbaloo Morango traz dois itens essenciais em nosso momento de autocuidado diário: Um hidratante com fragrância irresistível para cuidar da pele e um gloss com textura deliciosa. Essa dupla vem com o Cheirinho de Bubbaloo Morango.',
      preco: 100.80,
      img: 'https://res.cloudinary.com/beleza-na-web/image/upload/w_1500,f_auto,fl_progressive,q_auto:eco,w_800/v1/imagens/products/B2022081209/B2022081209_CBEM_BUBBALOO-MOR_HID_CPO_200ML_GLOSS.jpg',
    },
    {
      id: 2,
      nome: 'Combo Cereja Livre',
      resumo: 'Body Splash 200ml + Loção Corporal 400ml.',
      resenha: ' Com o Combo Cuide-se Bem Cereja Livre, você terá uma experiência única de cuidado e beleza com a fragrância suave e deliciosa da cereja. Ele combina produtos que proporcionam hidratação, frescor e uma sensação de leveza.',
      preco: 154.80,
      img: 'https://res.cloudinary.com/beleza-na-web/image/upload/w_1500,f_auto,fl_progressive,q_auto:eco,w_800/v1/imagens/product/B2025030422/32f7ad61-6a27-4f40-8145-a72de53a83df-bot-2025030422.jpg',
    },
    {
      id: 3,
      nome: 'Creme Desodorante Hidratante Corporal',
      resumo: 'Liz 100ml.',
      resenha: 'O Creme Desodorante Hidratante Corporal Liz é o item para pele que completa sua rotina ou ocasião especial. Trazendo todo cuidado que seu corpo precisa e potencializa a fragrância feminina e leve de Liz com hidratação indescritível.',
      preco: 35.90,
      img: 'https://res.cloudinary.com/beleza-na-web/image/upload/w_1500,f_auto,fl_progressive,q_auto:eco,w_800/v1/imagens/product/B52723/11613660-b4d4-4f18-bada-80d29fba7593-bot-52723-liz-creme-hidratante-frontal-1.jpg',
    },
    {
      id: 4,
      nome: 'Loção Desodorante Hidratante Corporal',
      resumo: 'Cuide-se Bem Boa Noite 200ml.',
      resenha: 'A Loção Desodorante Hidratante Corporal Cuide-se Bem Boa Noite é ideal para complementar a sua rotina de cuidados pessoais e te preparar para uma noite de sono tranquila. Afinal, ter um sono relaxante faz toda a diferença para cuidar do corpo e da mente.',
      preco: 49.90,
      img: 'https://res.cloudinary.com/beleza-na-web/image/upload/w_1500,f_auto,fl_progressive,q_auto:eco,w_800/v1/imagens/products/B82034/82034.jpg',
    },
    {
      id: 5,
      nome: 'Combo Cuide-se Bem Feira Cuidados Faciais',
      resumo: 'Gel de Limpeza Tangerina 150g + Hidratante Cremoso Banana 80g + Máscara Facial Noturna Melancia 50g.',
      resenha: 'Com Cuide-se Bem Feira, a feira é diferente, está em toda parte, vai com você aonde você for, no dia e na hora que você quiser! O Combo Cuide-se Bem Feira Cuidados Faciais proporciona uma mistura de frutas tropicais para um skincare com diferentes fragrâncias, texturas e novas maneiras de se amar.',
      preco: 111.90,
      img: 'https://res.cloudinary.com/beleza-na-web/image/upload/w_1500,f_auto,fl_progressive,q_auto:eco,w_1800,c_limit/e_trim/v1/imagens/product/B2024010205/1d1b5157-820c-4140-bd79-b9bbb7318c76-bot-2024010205-cuide-se-bem-feira-tangerina-gel-limpeza-facial-melancia-mascara-noturna-banana-creme-facial.jpg',
    },
    {
      id: 6,
      nome: 'Desodorante Colônia',
      resumo: 'Glamour Secrets Black 75ml.',
      resenha: 'Combinando diferentes flores, como a Flor de Tiaré, e frutas vermelhas, como a Framboesa, Glamour Secrets Black Desodorante Colônia traz um leve toque de Baunilha impossível de se resistir.',
      preco: 174.90,
      img: 'https://res.cloudinary.com/beleza-na-web/image/upload/w_1500,f_auto,fl_progressive,q_auto:eco,w_800/v1/imagens/products/B74103/GLAMOUR-DES-COL-SEC-BL-75ml-V4_B74103_frontal.jpg',
    },
    {
      id: 7,
      nome: 'Combo Boti Baby Lua',
      resumo: 'Colônia Para Bebê 100ml + Loção Corporal Banho e Pós-Banho 200ml.',
      resenha: 'Criar um ritual de cuidados noturno para o seu bebê é essencial para uma noite de sono tranquila e reparadora. Com o Combo Boti Baby Lua, você proporciona um momento de carinho e relaxamento, além de um cheirinho delicioso que acalma e aconchega.',
      preco: 154.80,
      img: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS4kwVklJr4na3vh4jO8G-sqk7DcyNOxQiWlg&s',
    },
  ]
)


const carrinho = ref
(
  {
    itens: 
    [
      {
        id: 4,
        nome: 'Loção Desodorante Hidratante Corporal',
        resumo: 'Cuide-se Bem Boa Noite 200ml',
        preco: 49.90,
        img: 'https://res.cloudinary.com/beleza-na-web/image/upload/w_1500,f_auto,fl_progressive,q_auto:eco,w_800/v1/imagens/products/B82034/82034.jpg',
        quantidade: 1,
        valorTotal: 49.90
      },
    ],
    frete: 0,
    desconto: 0,
    totalCompra: 0,
}
)


let idSugestao = Math.random(1, 7);

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

  <main>

    <section class="lancamentos">
      <h1>
        Lançamentos
      </h1>
      <div class="produtos">
        <div v-for="(produto, index) in produtos" :key="produto.id">
            <img :src="produto.img" :alt="produto.nome" width="100">
            <h2>
              {{ produto.nome }}
            </h2>
            <p>
              {{ produto.resumo }}
            </p>
            <div>
              <p>
                <span>R$</span>{{ produto.preco.toFixed(2).replace(".",",") }}
              </p>
              <p class="coracao">
                <span class="fa-regular fa-heart"></span>
              </p>
            </div>
            <p @click="adicionarCarrinho(produto, index)" class="botao">
              <span class="fa-solid fa-cart-shopping"></span> Comprar
            </p>
        </div>
      </div>

    </section>

    <section class="carrinho">

      <h1>
        Carrinho
      </h1>

      <div class="titulo">
        <h2>
          Nome do Produto
        </h2>
        <h2>
          Quantidade
        </h2>
        <h2>
          Subtotal
        </h2>
      </div>
      <div v-for="(compra, index) in carrinho.itens" class="compra">
        <div class="itens">
          <img :src="compra.img" :alt="compra.nome" width="100">
          <div>
            <h2>
            {{ compra.nome }}
           </h2>
           <p>
            {{ compra.resumo }}
           </p>
           <p>
            <span>R$</span> {{ compra.preco.toFixed(2).replace(".",",") }}
           </p>
          </div>
        </div>
        <div class="contador">
          <p>
            <button @click="incrementar(compra, index)">+</button>
            {{ compra.quantidade }}
            <button @click="decrementar(compra, index)">-</button>
          </p>
        </div>
        <div class="total">
          <p>
            <span>R$</span> {{ compra.valorTotal.toFixed(2).replace(".",",") }}
          </p>
        </div>
      </div>
      <button>
        Voltar para loja
      </button>
      
      <div>
        <div>
          <form action="">
            <p>
              <input type="text" v-model="input" placeholder="Código do Cupom"/>
              <button>
              Inserir Cupom
              </button>
            </p> 
          </form>
        </div>
      <div>
        <h2>
          Total da Compra
        </h2>
        <ul>
          <li>
            Produtos:
          </li>
          <li>
            <span>R$</span> {{ totalCompra }}
          </li>
        </ul>
        <ul>
          <li>
            Frete:
          </li>
          <li>
            Grátis
          </li>
        </ul>
        <ul>
          <li>
            Total:
          </li>
          <li>
            {{ (carrinho.totalCompra + carrinho.frete - carrinho.desconto).toFixed(2).replace(".",",") }}
          </li>
        </ul>
        <button>
          Ir para o pagamento
        </button>
      </div>
    </div>

    </section>
  </main>
  
</template>

<style src="./assets/reset.css">
</style>

<style scoped>

</style>
