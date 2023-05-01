<template>
  <div class="page">
    <Hero />
    <Registration />
    <GoOlcha />
    <Partners />
    <Installment />
    <Faq />
  </div>
</template>

<script>
import MyButton from "~/components/UI/MyButton";
import Hero from "~/components/mainPage/Hero";
import Registration from "~/components/mainPage/Registration";
import GoOlcha from "~/components/mainPage/GoOlcha";
import Partners from "@/components/mainPage/Partners";
import Installment from "@/components/mainPage/Installment";
import Faq from "@/components/mainPage/Faq";
export default {
  name: 'IndexPage',
  components: {Faq, Installment, Partners, GoOlcha, Registration, Hero, MyButton}
}
</script>

<style lang="scss">
@import "@/assets/styles/style";
</style>
