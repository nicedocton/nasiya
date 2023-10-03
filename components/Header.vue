<template>
  <header class="header">
    <div class="header__container _container">
      <button class="burger">
        <div>
          <span></span>
          <span></span>
          <span></span>
        </div>
      </button>
      <nuxt-link to="/" class="header__logo">
        <img src="@/assets/img/logo.svg" alt="olcha nasiya" />
      </nuxt-link>
      <nav class="header__nav">
        <ul>
          <li><nuxt-link to="/installment-terms">Условия рассрочки</nuxt-link></li>
          <li><nuxt-link to="/sell-on-olcha">Стать партнером</nuxt-link></li>
        </ul>
      </nav>
      <div class="header__actions">
        <LangSwitcher />
        <MyButton>Войти</MyButton>
        <MyButton class="btn__red">Зарегистрироваться</MyButton>
      </div>
    </div>
  </header>
</template>

<script>
import MyButton from "~/components/UI/MyButton";
export default {
  name: 'Header',
  components: {MyButton}
}
</script>

<style lang="scss" scoped>
@import "assets/styles/header";
</style>
