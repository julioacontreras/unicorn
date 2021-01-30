<template>
  <nuxt-link :to="to" class="hover:underline cursor-pointer">
    {{ title }}
  </nuxt-link>
</template>

<script>
export default {
  props: {
    to: {
      type: String,
      default: ''
    },
    title: {
      type: String,
      default: ''
    }
  }
}
</script>
