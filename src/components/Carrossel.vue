<template>
  <div>
    <div class="separador">
      <div class="linha"></div>
      <h2 class="blog__titulo">{{ tituloSecao }}</h2>
      <div class="linha"></div>
    </div>
    <q-carousel
        v-model="slide"
        transition-prev="slide-right"
        transition-next="slide-left"
        swipeable
        animated
        control-color="dark"
        control-type="regular"
        navigation
        padding
        infinite
        :autoplay="autoplay"
        arrows
        @mouseenter="autoplay = false"
        @mouseleave="autoplay = true"
        height="100%"
        class=""
      >
        <q-carousel-slide :name="1" class="">
          <div class="row fit justify-around items-center q-gutter-xs q-col-gutter">
            <q-card
            class="my-card carrossel__card"
            v-for="produtos in produtosCards"
            :key="produtos"
            v-bind="produtos"
            >
              <img src="~/src/assets/produto1.png" class="carrossel__card__imagem">
              <q-card-section class="carrossel__card__textos">
                <p class="carrossel__card__textos--titulo">{{ produtos.tituloProduto }}</p>
                <p class="carrossel__card__textos--descricao">{{ produtos.descricaoProduto }}</p>
                <p class="carrossel__card__textos--preco">{{ produtos.precoProduto }}</p>
              </q-card-section>
            </q-card>
          </div>
        </q-carousel-slide>
        <q-carousel-slide :name="2" class="column no-wrap">
          <div class="row fit justify-around items-center q-gutter-xs q-col-gutter">
            <q-card
            class="my-card carrossel__card"
            v-for="produtos in produtosCards"
            :key="produtos"
            v-bind="produtos"
            >
              <img src="~/src/assets/produto1.png" class="carrossel__card__imagem">
              <q-card-section class="carrossel__card__textos">
                <p class="carrossel__card__textos--titulo">{{ produtos.tituloProduto }}</p>
                <p class="carrossel__card__textos--descricao">{{ produtos.descricaoProduto }}</p>
                <p class="carrossel__card__textos--preco">{{ produtos.precoProduto }}</p>
              </q-card-section>
            </q-card>
          </div>
        </q-carousel-slide>
    </q-carousel>
  </div>
</template>

<script>
const produtosCards = [
  {
    tituloProduto: 'Ovo de Páscoa de Paçoca',
    descricaoProduto: 'Lorem ipsum dolor',
    precoProduto: 'R$ 65,00',
    imgProduto: ''
  },
  {
    tituloProduto: 'Chantighee com Wasabi 200g',
    descricaoProduto: 'Lorem ipsum dolor',
    precoProduto: 'R$ 32,00',
    imgProduto: '~/src/assets/produto2.png'
  },
  {
    tituloProduto: 'Shampoo Sólido Namah',
    descricaoProduto: 'Lorem ipsum dolor',
    precoProduto: 'R$ 49,00',
    imgProduto: '~/src/assets/produto3.png'
  },
  {
    tituloProduto: 'Condicionador Namah',
    descricaoProduto: 'Lorem ipsum dolor',
    precoProduto: 'R$ 69,00',
    imgProduto: '~/src/assets/produto4.png'
  }
]
export default {
  data () {
    return {
      autoplay: true,
      tituloSecao: 'Namah Shop',
      slide: 1,
      props: {
        tituloProduto: {
          type: String,
          required: true
        },
        descricaoProduto: {
          type: String,
          required: true
        },
        precoProduto: {
          type: String,
          required: true
        },
        imgProduto: {
          type: String,
          required: true
        }
      },
      produtosCards: produtosCards
    }
  }
}
</script>
