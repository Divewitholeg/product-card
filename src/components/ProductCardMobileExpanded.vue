<script setup lang="ts">
import ProductCardMobileLayoutVue from './ProductCardMobileLayout.vue'
defineProps<{
  prod: {
    title: string
    text: string[]
  }
}>()
</script>
<template>
  <ProductCardMobileLayoutVue :active="true">
    <template #caption>
      {{ prod.title }}
    </template>
    <template #text
      ><div v-for="p in prod.text" :key="p" class="m-2 p-2">{{ p }}</div></template
    >
  </ProductCardMobileLayoutVue>
</template>
