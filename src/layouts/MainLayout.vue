<template>
   <q-layout view="lHh Lpr lff">
    <q-header elevated>
      <q-toolbar class="navbar container">
        <div class="gt-sm">
          <q-list>
                <MenuLinks
                  v-for="link in linksMenu"
                  :key="link.title"
                  v-bind="link"
                />
          </q-list>
        </div>
        <img src="~/src/assets/logo.png" class="navbar__logo" lazy="loading" />
        <div class="navbar__icones col-4">
          <img
            src="~/src/assets/search-icon.png"
            class="navbar__icones--icon gt-sm"
            lazy="loading"
          />
          <img
            src="~/src/assets/user-icon.png"
            class="navbar__icones--icon"
            lazy="loading"
          />
          <img
            src="~/src/assets/package-icon.png"
            class="navbar__icones--icon gt-sm"
            lazy="loading"
          />
          <img
            src="~/src/assets/heart-icon.png"
            class="navbar__icones--icon"
            lazy="loading"
          />
          <img
            src="~/src/assets/basket-icon.png"
            class="navbar__icones--icon"
            lazy="loading"
          />
          <img
            src="~/src/assets/out-icon.png"
            class="navbar__icones--icon gt-sm"
            lazy="loading"
          />
        </div>
        <div class="lt-md">
            <q-btn
            flat
            dense
            round
            icon="menu"
            aria-label="Menu"
            @click="leftDrawerOpen = !leftDrawerOpen"
          />
        </div>
      </q-toolbar>
    </q-header>
        <q-drawer
            v-model="leftDrawerOpen"
            bordered
            content-class="bg-grey-1"
          >
          <q-list>
            <q-item-label
              header
              class="text-grey-8"
            >
            Menu
              </q-item-label>
              <MenuLinks
                v-for="link in linksMenu"
                :key="link.title"
                v-bind="link"
              />
          </q-list>
        </q-drawer>
    <q-page-container class="body">
      <Newsletter/>
    </q-page-container>
    <q-footer elevated class="footer">
        <div class="text-center">
          <div class="">
            <h2 class="footer__titulo">Assine nossa newsletter</h2>
            <div class="footer__desktop--top">
              <div class="footer__form">
                <input placeholder="Seu endereço de e-mail">
                <button>Assinar</button>
              </div>
              <hr class="footer__hr--mob--1">
              <img src="~/src/assets/footer-logo.png" class="footer__logo" lazy="loading" />
              <div class="footer__social">
                <img
                src="~/src/assets/rs-facebook.png"
                class="footer__social--icon"
                lazy="loading"
                />
                <img
                src="~/src/assets/rs-instagram.png"
                class="footer__social--icon"
                lazy="loading"
                />
                <img
                src="~/src/assets/rs-twitter.png"
                class="footer__social--icon"
                lazy="loading"
                />
              </div>
              <hr class="footer__hr--mob--2">
              <div class="row no-wrap justify-center footer__uls">
                <ul class="footer__ul">
                  <li class="text-bold">Institucional</li>
                  <li><a>Sobre nós</a></li>
                  <li><a>Contato</a></li>
                </ul>
                <ul class="footer__ul">
                  <li class="text-bold">Loja</li>
                  <li><a>Cadastre-se</a></li>
                  <li><a>Área do lojista</a></li>
                </ul>
                <ul class="footer__ul">
                  <li class="text-bold">Atendimento</li>
                  <li><a href="mailto:hello@espaconamah.com.br">hello@espaconamah.com.br</a></li>
                  <li><a href="tel:+553125156200">(31) 2515 6200</a></li>
                </ul>
              </div>
            </div>
          </div>
          <hr class="footer__hr--desk">
          <div class="footer__desktop--bottom">
            <div class="row footer__pagamento">
                  <p class="">Formas de pagamento</p>
                  <img
                  src="~/src/assets/pag-um.png"
                  class=""
                  lazy="loading"
                  />
                  <img
                  src="~/src/assets/pag-dois.png"
                  class=""
                  lazy="loading"
                  />
                  <img
                  src="~/src/assets/pag-tres.png"
                  class=""
                  lazy="loading"
                  />
                  <img
                  src="~/src/assets/pag-quatro.png"
                  class=""
                  lazy="loading"
                  />
                  <img
                  src="~/src/assets/pag-cinco.png"
                  class=""
                  lazy="loading"
                  />
            </div>
            <hr class="footer__hr--mob--3">
            <div class="row justify-center footer__infos">
              <p class="q-pr-sm"><span>&#128274;</span> Site seguro</p>
              <p class="q-pr-sm"> Site por <span class="text-bold">BIG BANG SHOP</span></p>
              <p>
                <a>Dúvidas frequentes</a>
                  |
                <a>Políticas da loja</a>
              </p>
            </div>
            <hr class="footer__hr--mob--4">
            <p class="footer__copyright">
              © 2020 Espaço Namah. Todos os direitos reservados.
              <br>
              CNPJ: 19.035.854/0001-31.
            </p>
          </div>
        </div>
    </q-footer>
  </q-layout>

</template>
<script>
import MenuLinks from 'components/MenuLinks.vue'
import Newsletter from 'components/Newsletter.vue'
const linksMenu = [
  {
    title: 'INÍCIO',
    link: ''
  },
  {
    title: 'BLOG',
    link: ''
  },
  {
    title: 'LOJA',
    link: ''
  },
  {
    title: 'PODCASTS',
    link: ''
  },
  {
    title: 'CURSOS',
    link: ''
  },
  {
    title: 'CONTATO',
    link: ''
  }
]

export default {
  name: 'MainLayout',
  components: { MenuLinks, Newsletter },
  data () {
    return {
      leftDrawerOpen: false,
      linksMenu: linksMenu
    }
  }
}
</script>
