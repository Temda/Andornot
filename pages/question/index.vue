<script setup lang="ts">
interface Cards {
  title: string;
  image: string;
  to: string;
}

const cards: Cards[] = [
  { title: "Free Question", image: "https://picsum.photos/seed/picsum/200/300", to: '/question/1' },
  { title: "Noob Question", image: "https://picsum.photos/seed/picsum/200/300", to: '/question/2' },
  { title: "Event Question", image: "https://picsum.photos/seed/picsum/200/300", to: '/question/3' },
];
</script>

<template>
<div class="max-w-7xl px-4 sm:px-6 lg:px-8 mx-auto w-full h-full mt-20">
  <div class="flex flex-col text-center w-full mb-20">
    <div class="basis-1/4 my-auto relative py-10 mt-10">
      <h1 class="font-bold text-4xl">Type of Question</h1>
    </div>
    <div class="basis-1/4 my-auto relative py-10 mt-10">
      <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-2 lg:grid-cols-3 gap-4">
          <NuxtLink v-for="(card, index) of cards" :key="index" :to="card.to">
            <div class="flex flex-col bg-white rounded-lg shadow-lg overflow-hidden hover:bg-gray-300">
              <div class="h-72 bg-gray-400 bg-cover bg-center"></div>
              <div class="p-6">
                <h3 class="text-xl font-semibold mb-2">{{ card.title }}</h3>
              </div>
            </div>
          </NuxtLink>
        </div>
    </div>
  </div>
</div>
</template>