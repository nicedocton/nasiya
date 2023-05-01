<template>
  <div
    class="accardion"
  >
    <div
      v-for="(item, index) in content"
      class="accardion__item"
      :class="{'is-active': currentFaq === index}"
      :key="item.id"
    >
      <div class="accardion__item-title" @click="faqTrigger(index)">
        <span
          class="accardion-caret"
          :class="{'is-active': currentFaq === index}"
        />
        <span>{{ item.title }}</span>
      </div>
      <transition
        mode="out-in"
        name="faq-fade"
        v-on:before-enter="beforeEnterFaq"
        v-on:enter="enterFaq"
      >
        <div
          v-show="currentFaq === index"
          class="accardion__item-details"
        >
          <div class="accardion__item-details-inner">
            {{ item.details }}
          </div>
        </div>
      </transition>
    </div>
  </div>
</template>

<script setup lang="ts">

import {ref} from "vue";

const currentFaq = ref(-10);

const props = defineProps({
  content: {
    type: Array,
    required: true,
    default: false
  }
});

function faqTrigger(newFaq) {
  if (newFaq === currentFaq.value) {
    currentFaq.value = -10
  } else {
    currentFaq.value = newFaq
  }
}

function beforeEnterFaq(_t) {
  _t.style.display = 'block'
  _t.style.maxHeight = null
  _t.myHeight = _t.offsetHeight
  _t.style.maxHeight = 0
  _t.style.display = null
}

function enterFaq(_t) {
  _t.style.maxHeight = _t.myHeight + 'px'
}

</script>

<style scoped lang="scss">
@import "@/assets/styles/UI/accardion"
</style>
