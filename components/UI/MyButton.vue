<template>
  <button class="btn">
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: 'MyButton'
}
</script>

<style lang="scss" scoped>
@import "@/assets/styles/UI/btn"
</style>
