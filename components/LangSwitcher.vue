<template>
  <div
    ref="langList"
    class="header__lang lang"
    :class="{'_active': isActive }"
  >
    <button class="lang__btn" @click="isActive = !isActive">
      <img src="@/assets/img/svg/ru.svg" alt="" />
      <span>{{ locales[0].name }}</span>
    </button>
    <ul v-show="isActive">
      <li>
        <a
          href="#"
          v-for="lang in locales"
          @click.stop="selectLocale"
          :key="lang.code"
        >
          <img src="@/assets/img/svg/ru.svg" alt="" />
          <span>{{ lang.name }}</span>
        </a>
      </li>
    </ul>
  </div>
</template>

<script lang="ts" setup>
import {ref, watch} from 'vue';

const isActive = ref(false);
const langList = ref(null)

const locales = [
  {
    name: 'Рус',
    img: 'ru.svg',
    code: 'ru'
  },
  {
    name: 'Uzb',
    img: 'ru.svg',
    code: 'uz'
  },
  {
    name: 'Eng',
    img: 'ru.svg',
    code: 'en'
  }
]

watch(isActive, (newVal) => {
  if (newVal) {
    window.addEventListener('click', clickOutSide)
  } else {
    window.removeEventListener('click', clickOutSide)
  }
})

function clickOutSide (e) {
  if (!langList.value.contains(e.target)) {
    isActive.value = false
  }
}

function selectLocale () {
  isActive.value = false
}

</script>

<style scoped lang="scss">
@import "assets/styles/langSwiTcher";
</style>
