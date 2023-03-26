<script setup lang="ts">
import ProductCardMobileLayoutVue from './ProductCardMobileLayout.vue'
defineProps<{
  prod: {
    slogan: string
    price: string
  }
}>()
</script>
<template>
  <ProductCardMobileLayoutVue :active="false">
    <template #caption>
      {{ prod.slogan }}
    </template>
    <template #text>{{ prod.price.slice(-13) }}</template>
  </ProductCardMobileLayoutVue>
</template>
