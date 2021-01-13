<template>
  <div class="blog">
    <div class="separador">
      <div class="linha"></div>
      <h2 class="blog__titulo">{{titulo}}</h2>
      <div class="linha"></div>
    </div>
    <div class="row justify-between">
      <q-card class="my-card--lg q-mb-md oi">
          <q-img src="~/src/assets/blog-card1.png">
            <div class="absolute-bottom">
              <h4 class="blog__card__titulo">{{lorem}}</h4>
              <div class="row">
                <p class="blog__card__tag">Viagem</p>
                <p class="blog__card__autor">Fulano de tal</p>
              </div>
            </div>
          </q-img>
      </q-card>
      <q-card class="my-card--lg q-mb-md oi">
          <q-img src="~/src/assets/blog-card2.png">
            <div class="absolute-bottom">
              <h4 class="blog__card__titulo">{{lorem}}</h4>
              <div class="row">
                <p class="blog__card__tag">Desenvolvimento pessoal</p>
                <p class="blog__card__autor">Fulano de tal</p>
              </div>
            </div>
          </q-img>
      </q-card>
    </div>
    <div class="">
      <div class="q-mb-md blog__section__cards">
          <q-card class="my-card--sm">
              <img src="~/src/assets/blog-card3.png">
                <q-card-section>
                  <h4 class="blog__card__titulo--size">{{lorem}}</h4>
                  <p class="blog__card__tag">Viagem</p>
                </q-card-section>
              <q-card-section class="q-pt-none">
                  {{ loremTexto }}
              </q-card-section>
          </q-card>
          <q-card class="my-card--sm">
            <img src="~/src/assets/blog-card4.png">
              <q-card-section>
                <h4 class="blog__card__titulo--size">{{lorem}}</h4>
                <p class="blog__card__tag">Viagem</p>
              </q-card-section>
            <q-card-section class="q-p-none">
                {{ loremTexto }}
            </q-card-section>
          </q-card>
          <Newsletter class="blog__newsletter--desk"/>
      </div>
      <Newsletter class="blog__newsletter--mob"/>
    </div>
    <button class="blog__button">
      Veja todos os posts
      <span>&#129042;</span>
    </button>
  </div>
</template>
<script>
import Newsletter from 'components/Newsletter.vue'

export default {
  components: { Newsletter },
  data () {
    return {
      titulo: 'Blog',
      lorem: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit',
      loremTexto: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna...'
    }
  }
}
</script>
