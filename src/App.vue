<script setup lang="ts">
import { ref } from 'vue'
import ProductCardMobile from './components/ProductCardMobile.vue'
import ProductCardMobileExpanded from './components/ProductCardMobileExpanded.vue'
interface Product {
  name: string
  title: string
  slogan: string
  price: string
  text: string[]
}
const prod: Product = {
  name: 'blog',
  title: 'Personal Blog or Home-About-Contacts page',
  slogan: 'Showcase yourself with our Personal Blog or Home-About-Contacts page!',
  price: 'Includes 3 business days. Price: starting from 150 EUR.',
  text: [
    'Oleg Rõbnikov Web Development offers a Personal Blog or Home-About-Contacts page that is perfect for individuals or small businesses who want to showcase their personal brand or business information.',
    'I work with you to create a website with editable content that can be expanded into a content management system for your blogging or other publishing activities. The project only takes 3 business days and starts at a price of 150 EUR.',
    'I am dedicated to providing the best customer experience for my clients, and I take pride in delivering top-notch solutions that meet their specific needs.'
  ]
}
const active = ref(true)
</script>
<template>
  <div class="flex h-screen items-center wheelsBackground">
    <Transition
      mode="out-in"
      enter-from-class="duration-100 opacity-0 translate-y-5"
      enter-active-class="duration-300 opacity-30"
      enter-to-class="duration-200 opacity-100 rotate-180"
      leave-from-class="duration-100 opacity-100"
      leave-active-class="duration-200 opacity-50 "
      leave-to-class="duration-200 opacity-0 translate-y-5"
      appear
    >
      <ProductCardMobile v-if="active" @click="active = !active" :prod="prod" />
      <ProductCardMobileExpanded v-else @click="active = !active" :prod="prod" />
    </Transition>
  </div>
</template>
