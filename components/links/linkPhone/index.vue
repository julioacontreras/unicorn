<template>
  <a :href="'tel:' + to" class="hover:underline cursor-pointer">
    {{ title }}
  </a>
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
