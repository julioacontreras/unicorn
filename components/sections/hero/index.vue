<template>
  <div
    class="flex flex-col w-full bg-cover h-64 pt-20"
    :style="{'background-image': `url(${img})`}"
  >
    <div
      v-for="(item, idx) in items"
      :key="idx"
      :class="[
        {'justify-begin': textHrzSide === 'left'},
        {'justify-center': textHrzSide === 'center'},
        {'justify-end': textHrzSide === 'right'},
        {'text-4xl': !item.size},
        {'text-3xl': item.size === 'xl'},
        {'text-2xl': item.size === 'l'},
        {'text-base': item.size === 's'},
        {'text-sm': item.size === 'xs'},
        {'text-white': item.textColor === 'higlight'}
      ]"
      class="flex font-bold text-shadow-lg"
    >
      {{ item.text }}
    </div>
  </div>
</template>

<script>
export default {
  props: {
    img: {
      type: String,
      default: ''
    },
    textHrzSide: {
      type: String,
      default: 'left'
    },
    textVrtSide: {
      type: String,
      default: 'top'
    },
    items: {
      type: Array,
      default: () => []
    }
  }
}
</script>
