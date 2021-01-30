<template>
  <div>
    <video v-bind="props">
      <source v-if="mp4" :mp4="src" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>
</template>

<script>
export default {
  props: {
    mp4: {
      type: String,
      default: ''
    },
    props: {
      type: Object,
      default: () => {}
    }
  }
}
</script>
