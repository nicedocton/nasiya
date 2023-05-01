<template>
  <section class="section hero">
    <div class="hero__container _container">
      <div class="hero__content">
        <div class="hero__title">Как <span>зарегистрироваться?</span> всего за пару кликов</div>
        <div class="hero__text">
          Зарегистрируйтесь на сайте всего за несколько минут и получите мгновенный доступ к рассрочке необходимых товаров с лимитом до 15 миллионов сум.
        </div>
        <MyButton class="btn__red">Регистрация</MyButton>
      </div>
    </div>
  </section>
</template>

<script>
import MyButton from "~/components/UI/MyButton";

export default {
  name: 'Hero',
  components: {MyButton}
}
</script>

<style scoped lang="scss">
@import "@/assets/styles/mainPage/hero";
</style>
