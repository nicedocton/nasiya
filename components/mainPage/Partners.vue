<template>
  <section class="section partners">
    <div class="partners__container _container">
      <div class="partners__title title">Наши партнеры</div>
      <div class="partners__list">
        <div
          v-for="item in partnersList"
          class="partners__item"
          :key="item.id"
        >
          <img :src="require(`@/assets/img/partners/${item.img}`)" />
        </div>
      </div>
      <div class="partners__btn-wrap">
        <MyButton class="btn__red">Все партнеры</MyButton>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import MyButton from "../UI/MyButton.vue";

const partnersList = [
  {
    id: 0,
    name: 'texnomart',
    img: 'texnomart.png'
  },
  {
    id: 1,
    name: 'mac bro',
    img: 'macbro.png'
  },
  {
    id: 2,
    name: 'goodzone',
    img: 'goodzone.png'
  },
  {
    id: 3,
    name: 'mediapark',
    img: 'mediapark.png'
  },
  {
    id: 4,
    name: 'elmakon',
    img: 'elmakon.png'
  },
  {
    id: 5,
    name: 'terra pro',
    img: 'terrapro.png'
  },
  {
    id: 6,
    name: 'radius',
    img: 'radius.png'
  },
  {
    id: 7,
    name: 'smart store',
    img: 'smartstore.png'
  },
  {
    id: 8,
    name: 'paragraf',
    img: 'paragraf.png'
  },
  {
    id: 9,
    name: 'idea',
    img: 'idea.png'
  }
]

</script>

<style scoped lang="scss">
@import "@/assets/styles/mainPage/partners"
</style>
