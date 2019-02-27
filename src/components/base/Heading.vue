<template>
  <component
    :is="tag"
    class="v-heading mb-3"
  >
    <slot />
  </component>
</template>

<script>
export default {
  props: {
    tag: {
      type: String,
      default: 'h1'
    }
  }
}
</script>

<style lang="sass">
  .v-heading
    font-family: "Montserrat",sans-serif
    font-weight: bold
    font-size: 64px
    line-height: 1.1
</style>
