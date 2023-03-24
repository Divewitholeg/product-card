<script setup lang="ts">
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
    'Oleg Rõbnikov Web Development offers a Personal Blog or Home-About-Contacts page that is perfect for individuals or small businesses who want to showcase their personal brand or business information. I work with you to create a website with editable content that can be expanded into a content management system for your blogging or other publishing activities. The project only takes 3 business days and starts at a price of 150 EUR. I am dedicated to providing the best customer experience for my clients, and I take pride in delivering top-notch solutions that meet their specific needs.'
  ]
}
</script>
<template>
  <div
    class="flex items-center mx-auto h-[20vh] w-[80vw] bg-gradient-to-r from-rose-400 via-fuchsia-500 to-indigo-500 rounded-lg transform -rotate-6"
  >
    <div
      class="relative mx-auto [&>div]:my-3 [&>div]:leading-7 h-[18vh] w-[75vw] bg-gradient-to-r from-rose-100 to-teal-100 rounded-lg"
    >
      <div class="font-semibold font-sans px-2">
        <span
          class="text-xl tracking-tighter italic text-transparent bg-clip-text bg-gradient-to-l from-rose-400 via-fuchsia-500 to-indigo-500"
          >{{ prod.slogan }}</span
        >
      </div>
      <div class="text-lg ml-5 font-extralight">
        {{ prod.price.slice(-13) }}
      </div>
    </div>
  </div>
</template>
