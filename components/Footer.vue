<template>
  <footer class="footer">
    <div class="footer_container _container">
      <div class="footer-top">
        <div class="footer-top__col">
          <a href="#" class="footer__logo">
            <img src="@/assets/img/logo.svg" alt="" />
          </a>
          <div class="footer-top__phone">
            <span>Телефон поддержки</span>
            <a rel="nofollow" href="tel:998712022021" aria-label="998712022021">+998 (71) 202 202 1</a>
          </div>
          <div class="footer-top__geo">
            Козитарнов, Ташкент
          </div>
          <div class="footer-top__mail">
            <a rel="nofollow" href="mailto:info@olcha.uz" aria-label="info@olcha.uz">info@olcha.uz</a>
          </div>
        </div>
        <div class="footer-top__col">
          <div class="footer-top__list">
            <div class="footer-top__head">Для покупателей</div>
            <ul>
              <li>
                <a href="#">Условия рассрочки</a>
              </li>
              <li>
                <a href="#">Частые вопросы</a>
              </li>
              <li>
                <a href="#">Купить товар в <span>Olcha</span></a>
              </li>
            </ul>
          </div>
          <div class="footer-top__list">
            <div class="footer-top__head">Для партнеров</div>
            <ul>
              <li>
                <a href="#">Наши партнеры</a>
              </li>
              <li>
                <a href="#">Стать партнером</a>
              </li>
            </ul>
          </div>
        </div>
        <div class="footer-top__col">
          <div class="footer-top__payments">
            <a
              v-for="item in paymentTypes"
              rel="nofollow"
              :href="item.url"
              :aria-label="item.id"
              :key="item.id"
            >
              <img :src="require(`@/assets/img/payments/${item.img}`)" />
            </a>
          </div>
        </div>
      </div>
      <div class="footer-bottom">
        <div class="footer-bottom__col">
          <div class="footer-bottom__copy">
            &copy; 2023. ООО "Olcha Instalment"
          </div>
        </div>
        <div class="footer-bottom__col">
          <div class="footer-bottom__public">
            <a href="#" class="">
              Публичная оферта
            </a>
            <a href="#" class="">
              Политика конфиденциальности
            </a>
          </div>
        </div>
        <div class="footer-bottom__col">
          <div class="footer-bottom__socials">
            <a
              v-for="item in socialsList"
              :href="item.url"
              :aria-label="item.url"
              :key:="item.id"
            >
              <svg
                class="svg"
                width="32"
                height="32"
              >
                <use xlink:href="@/assets/img/svg/sprite.svg#facebook" />
<!--                <image :xlink:href="require(`@/assets/img/svg/${item.img}`)" />-->
              </svg>
            </a>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup lang="ts">
const paymentTypes = [
  {
    id: 'apelsin.uz',
    url: 'https://apelsin.uz',
    img: 'apelsin.svg'
  },
  {
    id: 'uzcard.uz',
    url: 'https://uzcard.uz/',
    img: 'uzcard.svg'
  },
  {
    id: 'click.uz',
    url: 'https://click.uz/',
    img: 'click.svg'
  },
  {
    id: 'payme.uz',
    url: 'https://payme.uz/',
    img: 'payme.svg'
  },
  {
    id: 'humocard.uz',
    url: 'https://humocard.uz/',
    img: 'humo.svg'
  },
  {
    id: 'paynet.uz',
    url: 'https://app.paynet.uz/?m=4633&c=14922',
    img: 'paynet.svg'
  },
]
const socialsList = [
  {
    id: 'facebook.com',
    url: 'https://www.facebook.com/olchauz/',
    img: 'facebook.svg'
  },
  {
    id: 'instagram.com',
    url: 'https://www.instagram.com/olcha_uz/',
    img: 'instagram.svg'
  },
  {
    id: 'telegram.me',
    url: 'https://t.me/olchauz',
    img: 'telegram.svg'
  }
]
</script>

<style scoped lang="scss">
@import "@/assets/styles/footer";
</style>
