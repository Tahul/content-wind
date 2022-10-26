<template>
  <component :is="as">
    <ContentSlot :use="$slots.default" unwrap="*" />
  </component>
</template>

<script setup lang="ts">
import { cssProp } from 'pinceau/runtime'

defineProps({
  as: {
    type: String,
    required: false,
    default: 'div'
  },
  css: cssProp
})
</script>

<style lang="ts">
css({
  variants: {
    padded: {}
  }
})
</style>
