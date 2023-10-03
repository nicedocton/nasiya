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
          <div class="footer-bottom__public">
            <a href="#" class="">
              Политика конфиденциальности
            </a>
            <a href="#" class="">
              Публичная оферта
            </a>
          </div>
        </div>
        <div class="footer-bottom__col">
          <div class="footer-bottom__socials">
            <a
              href="https://www.facebook.com/olchauz/"
              target="_blank"
              rel="noopener noreferrer"
            >
              <svg
                class="svg"
                width="32"
                height="32"
                viewBox="0 0 32 32"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path id="subtract" fill-rule="evenodd" clip-rule="evenodd" d="M4 16C4 21.9333 8.33333 26.8667 14 27.8667L14.0669 27.8132C14.0446 27.8088 14.0223 27.8045 14 27.8V19.3333H11V16H14V13.3333C14 10.3333 15.9333 8.66667 18.6667 8.66667C19.5333 8.66667 20.4667 8.8 21.3333 8.93333V12H19.8C18.3333 12 18 12.7333 18 13.6667V16H21.2L20.6667 19.3333H18V27.8C17.9777 27.8045 17.9554 27.8088 17.9331 27.8132L18 27.8667C23.6667 26.8667 28 21.9333 28 16C28 9.4 22.6 4 16 4C9.4 4 4 9.4 4 16Z" />
              </svg>
            </a>
            <a
              href="https://www.facebook.com/olchauz/"
              target="_blank"
              rel="noopener noreferrer"
            >
              <svg
                class="svg"
                width="32"
                height="32"
                viewBox="0 0 32 32"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path d="M16.0005 4.36377C12.8404 4.36377 12.4438 4.37759 11.2026 4.43407C9.96384 4.4908 9.11829 4.68692 8.37843 4.97468C7.61312 5.27189 6.96393 5.66947 6.31716 6.3165C5.66991 6.96328 5.27235 7.6125 4.97417 8.37759C4.6857 9.11771 4.48934 9.96353 4.43358 11.2018C4.37807 12.443 4.36353 12.8399 4.36353 16.0001C4.36353 19.1604 4.37759 19.5558 4.43383 20.797C4.49079 22.0358 4.68691 22.8813 4.97442 23.6212C5.27186 24.3866 5.66943 25.0358 6.31644 25.6826C6.96296 26.3298 7.61215 26.7284 8.37698 27.0256C9.11732 27.3133 9.96311 27.5095 11.2016 27.5662C12.4428 27.6227 12.8391 27.6365 15.9991 27.6365C19.1594 27.6365 19.5548 27.6227 20.796 27.5662C22.0347 27.5095 22.8813 27.3133 23.6216 27.0256C24.3867 26.7284 25.0349 26.3298 25.6814 25.6826C26.3287 25.0358 26.7262 24.3866 27.0244 23.6215C27.3105 22.8813 27.5068 22.0355 27.565 20.7972C27.6208 19.556 27.6353 19.1604 27.6353 16.0001C27.6353 12.8399 27.6208 12.4433 27.565 11.2021C27.5068 9.96328 27.3105 9.11771 27.0244 8.37783C26.7262 7.6125 26.3287 6.96328 25.6814 6.3165C25.0342 5.66922 24.3869 5.27165 23.6209 4.97468C22.8791 4.68692 22.0331 4.4908 20.7943 4.43407C19.5531 4.37759 19.158 4.36377 15.9969 4.36377H16.0005ZM14.9567 6.46074C15.2665 6.46025 15.6122 6.46074 16.0005 6.46074C19.1073 6.46074 19.4756 6.47189 20.7024 6.52765C21.8369 6.57953 22.4527 6.7691 22.8628 6.92838C23.4059 7.13928 23.793 7.39141 24.2 7.79868C24.6073 8.20595 24.8594 8.59383 25.0708 9.13686C25.23 9.54656 25.4199 10.1623 25.4715 11.2969C25.5272 12.5235 25.5394 12.892 25.5394 15.9975C25.5394 19.1029 25.5272 19.4714 25.4715 20.6981C25.4196 21.8326 25.23 22.4484 25.0708 22.8581C24.8599 23.4011 24.6073 23.7878 24.2 24.1948C23.7928 24.6021 23.4061 24.8542 22.8628 25.0651C22.4532 25.2251 21.8369 25.4142 20.7024 25.4661C19.4758 25.5218 19.1073 25.534 16.0005 25.534C12.8934 25.534 12.5252 25.5218 11.2986 25.4661C10.1641 25.4137 9.54834 25.2241 9.13793 25.0649C8.59491 24.854 8.20705 24.6018 7.79978 24.1946C7.39252 23.7873 7.14041 23.4004 6.92902 22.8571C6.76976 22.4474 6.57994 21.8316 6.52831 20.6971C6.47255 19.4704 6.4614 19.102 6.4614 15.9946C6.4614 12.8872 6.47255 12.5206 6.52831 11.294C6.58019 10.1594 6.76976 9.54365 6.92902 9.13347C7.13993 8.59044 7.39252 8.20256 7.79978 7.79528C8.20705 7.38801 8.59491 7.13589 9.13793 6.9245C9.5481 6.7645 10.1641 6.57541 11.2986 6.52328C12.372 6.4748 12.788 6.46025 14.9567 6.45783V6.46074ZM22.2117 8.39286C21.4408 8.39286 20.8154 9.01759 20.8154 9.78874C20.8154 10.5596 21.4408 11.1851 22.2117 11.1851C22.9826 11.1851 23.608 10.5596 23.608 9.78874C23.608 9.01783 22.9826 8.39238 22.2117 8.39238V8.39286ZM16.0005 10.0244C12.7005 10.0244 10.0249 12.7 10.0249 16.0001C10.0249 19.3003 12.7005 21.9747 16.0005 21.9747C19.3005 21.9747 21.9751 19.3003 21.9751 16.0001C21.9751 12.7 19.3003 10.0244 16.0003 10.0244H16.0005ZM16.0005 12.1213C18.1425 12.1213 19.8792 13.8578 19.8792 16.0001C19.8792 18.1422 18.1425 19.8789 16.0005 19.8789C13.8583 19.8789 12.1218 18.1422 12.1218 16.0001C12.1218 13.8578 13.8583 12.1213 16.0005 12.1213Z" fill="#999999" />
              </svg>
            </a>
            <a
              href="https://www.facebook.com/olchauz/"
              target="_blank"
              rel="noopener noreferrer"
            >
              <svg
                class="svg"
                width="32"
                height="32"
                viewBox="0 0 32 32"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path id="subtract" fill-rule="evenodd" clip-rule="evenodd" d="M24.4339 7.4839L5.16841 14.9146C3.8535 15.4422 3.8613 16.1756 4.92874 16.5026L9.73361 18.0023L11.5721 23.6389C11.7956 24.2558 11.6854 24.5005 12.3332 24.5005C12.8332 24.5005 13.0549 24.2725 13.3334 24.0005C13.5105 23.8273 14.5618 22.8051 15.7357 21.6638L20.7337 25.3565C21.6533 25.8639 22.3174 25.601 22.5464 24.5023L25.8272 9.04205C26.1631 7.69538 25.3138 7.08454 24.4339 7.4839ZM10.4877 17.6578L21.3179 10.8249C21.8585 10.497 22.3543 10.6733 21.9472 11.0346L12.6738 19.4016L12.3127 23.2528L10.4877 17.6578Z" fill="#999999" />
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
