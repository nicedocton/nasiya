<template>
  <section class="section go-olcha">
    <div class="go-olcha__container _container">
      <div class="go-olcha__content">
        <h2 class="go-olcha__title title">Вперед в <span>olcha!</span></h2>
        <div class="go-olcha__text">Приобретайте товары с удобной системой рассрочки в приложении или на сайте Olcha</div>
        <MyButton class="btn__red">Перейти в olcha</MyButton>
      </div>
    </div>
  </section>
</template>

<script>
import MyButton from "~/components/UI/MyButton";
export default {
  name: 'GoOlcha',
  components: {MyButton}
}
</script>

<style scoped lang="scss">
@import "@/assets/styles/mainPage/goOlcha";
</style>
