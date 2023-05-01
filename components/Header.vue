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
      <a href="#" class="header__logo">
        <img src="@/assets/img/logo.svg" alt="olcha nasiya" />
      </a>
      <nav class="header__nav">
        <ul>
          <li><a href="#">Условия рассрочки</a></li>
          <li><a href="#">Стать партнером</a></li>
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
