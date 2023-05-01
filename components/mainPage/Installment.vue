<template>
  <section class="section installment">
    <div class="installment__container">
      <div class="installment__content _container">

        <div class="installment-purchase">
          <h2 class="installment__title title">Покупка в рассрочку</h2>
          <div class="installment-purchase__list">
            <div
              v-for="item in purchaseList"
              class="installment-purchase__item"
              :key="item.id"
            >
              <div class="installment-purchase__item-icon">
                <span>
                  <img :src="require(`@/assets/img/svg/${item.icon}`)" />
                </span>
              </div>
              <div class="installment-purchase__item-text">
                <span>{{ item.title }}</span>
                {{ item.text }}
              </div>
            </div>
          </div>
        </div>

        <div class="installment-methods">
          <h2 class="installment__title title">Методы погашения рассрочки</h2>
          <div class="installment-methods__list">
            <div class="installment-methods__item methods-item">
              <div class="methods-item__icon">
                <span>
                  <img src="@/assets/img/logos/olcha.svg" alt="" />
                </span>
              </div>
              <div class="methods-item__title">
                Через приложение olcha pay
              </div>
              <div class="methods-item__text">
                Заходите в раздел Nasiya, выберите рассрочку и произведите оплату
              </div>
              <a href="#" class="link">Скачать</a>
            </div>
            <div class="installment-methods__item methods-item">
              <div class="methods-item__icon">
                <span>
                  <img src="@/assets/img/logos/apelsin.svg" alt="" />
                </span>
                <span>
                  <img src="@/assets/img/logos/click.svg" alt="" />
                </span>
                <span>
                  <img src="@/assets/img/logos/payme.svg" alt="" />
                </span>
              </div>
              <div class="methods-item__title">
                Через приложение
              </div>
              <div class="methods-item__text">
                Через другие мобильные приложения как: Payme, Click или Apelsin
              </div>
            </div>
            <div class="installment-methods__item methods-item">
              <div class="methods-item__icon">
                <span>
                  <img src="@/assets/img/logos/paynet.svg" alt="" />
                </span>
              </div>
              <div class="methods-item__title">
                Ближайщие банки
              </div>
              <div class="methods-item__text">
                Через Paynet или любые локальные банки
              </div>
            </div>
          </div>
        </div>

        <div class="installment-download">
          <div class="installment-download__content">
            <h2 class="installment-download__title title">Скачайте приложение и оформляйте рассрочку</h2>
            <div
              class="installment-download__list"
            >
              <a
                v-for="store in stores"
                :href="store.url"
                :key="store.id"
              >
                <img :src="require(`@/assets/img/logos/${store.img}`)" alt="" />
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
const purchaseList = [
  {
    id: '0',
    icon: 'u_plus-circle.svg',
    title: 'Выберите товар в магазине наших партнеров',
    text: 'Сообщите продавцу, что вы хотите приобрести товар на условиях рассрочки через сервис Olcha Nasiya.'
  },
  {
    id: '1',
    icon: 'u_file-check-alt.svg',
    title: 'Выбираете удобные вам условия',
    text: 'Выберите наиболее подходящий для вас срок рассрочки и сообщите об этом продавцу-консультанту. '
  },
  {
    id: '2',
    icon: 'u_file-download-alt.svg',
    title: 'Оформляете рассрочку на выбранный товар',
    text: 'Ознакомьтесь с условиями рассрочки и подтвердите покупку SMS-кодом, который придет на ваш  номер телефона.'
  },
  {
    id: '3',
    icon: 'u_favorite.svg',
    title: 'Пользуетесь с товаром',
    text: 'Забирайте и пользуйтесь товаром, и оплачивайте позже по графику.'
  }
]
const stores = [
  {
    id: 'appstore',
    img: 'appstore.png',
    url: 'https://apps.apple.com/uz/app/olcha/id1551492785'
  },
  {
    id: 'googleplay',
    img: 'googleplay.png',
    url: 'https://play.google.com/store/apps/developer?id=Olcha+LLC'
  },
  {
    id: 'appgallery',
    img: 'appgallery.png',
    url: 'https://appgallery.huawei.com/app/C105125705'
  }
]
</script>

<style scoped lang="scss">
@import "@/assets/styles/mainPage/installment";
</style>
