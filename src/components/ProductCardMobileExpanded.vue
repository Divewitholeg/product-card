<script setup lang="ts">
defineProps<{
  prod: {
    name: string
    title: string
    slogan: string
    price: string
    text: string[]
  }
}>()
</script>
<template>
  <div
    class="flex items-center mx-auto px-1 h-[70vh] w-[80vw] bg-gradient-to-r from-rose-400 via-fuchsia-500 to-indigo-500 rounded-lg shadow-slate-500 shadow-lg"
  >
    <div
      class="overflow-y-scroll relative mx-auto [&>div]:my-3 [&>div]:leading-7 h-[68vh] w-[75vw] bg-gradient-to-r from-rose-100 to-teal-100 shadow-white shadow-inner rounded-lg"
    >
      <div
        class="animate-[bounce_0.5s_ease-in] font-semibold font-sans px-2 -indent-2"
        style="animation-iteration-count: 3"
      >
        <span
          class="text-xl tracking-tighter italic text-transparent bg-clip-text bg-gradient-to-l from-rose-400 via-fuchsia-500 to-indigo-500 px-2"
        >
          {{ prod.title }}
        </span>
      </div>
      <div v-for="p in prod.text" :key="p" class="p-2 m-2">
        <p>{{ p }}</p>
      </div>
    </div>
  </div>
</template>
