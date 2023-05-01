<template>
  <section class="section faq">
    <div class="faq__container _container">
        <div class="faq__aside">
          <h2 class="faq__title title">Часто задаваемые вопросы</h2>
          <MyButton class="btn__red">Задать вопрос</MyButton>
        </div>
        <div class="faq__content">
          <Accardion
            :content="content"
          />
        </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import MyButton from "@/components/UI/MyButton";
import Accardion from "../UI/Accardion.vue";

const content = [
  {
    id: 1,
    title: 'Как я могу погасить рассрочку?',
    details: "Регистрация в системе Olcha Nasiya полностью бесплатная."
  },
  {
    id: 2,
    title: 'Сколько стоит пройти регистрацию?',
    details: "Регистрация в системе Olcha Nasiya полностью бесплатная. " +
      "Регистрация в системе Olcha Nasiya полностью бесплатная. " +
      "Регистрация в системе Olcha Nasiya полностью бесплатная."
  },
  {
    id: 3,
    title: `Как начать пользоваться сервисом?`,
    details: "Регистрация в системе Olcha Nasiya полностью бесплатная. " +
      "Регистрация в системе Olcha Nasiya полностью бесплатная.\""
  },
  {
    id: 4,
    title: 'По каким причинам получают отказ при регистрации?',
    details: "Регистрация в системе Olcha Nasiya полностью бесплатная."
  },
  {
    id: 5,
    title: 'Можно ли пройти повторную регистрацию, если ранее было отказано?',
    details: "Регистрация в системе Olcha Nasiya полностью бесплатная. " +
      "Регистрация в системе Olcha Nasiya полностью бесплатная. " +
      "Регистрация в системе Olcha Nasiya полностью бесплатная."
  },
  {
    id: 6,
    title: `Какую пластиковую карту нужно указывать при регистрации?`,
    details: "Регистрация в системе Olcha Nasiya полностью бесплатная. " +
      "Регистрация в системе Olcha Nasiya полностью бесплатная.\""
  }
]

</script>

<style scoped lang="scss">
@import '@/assets/styles/mainPage/faq'
</style>
