<script setup lang="ts">
interface Cards {
  title: string;
  image: string;
  to: string;
}

const cards: Cards[] = [
  { title: "Halloween", image: "https://th-images.hellomagazine.com/wp-content/uploads/2021/10/28114948/4183289-1024x683.jpg", to: '/event/1' },
  { title: "Christmas", image: "https://www.history.com/.image/t_share/MTY4ODE4ODA4MzY1MDAwNDY1/christmas-gettyimages-184652817.jpg", to: '/event/2' },
  { title: "Valentine", image: "https://www.daysoftheyear.com/wp-content/uploads/valentines-day-concept-2021-12-14-20-37-41-utc-scaled.jpg", to: '/event/3' },
];
</script>

<template>
<div class="max-w-7xl px-4 sm:px-6 lg:px-8 mx-auto w-full h-full mt-20">
  <div class="flex flex-col text-center w-full mb-20">
    <div class="basis-1/4 my-auto relative py-10 mt-10">
      <h1 class="font-bold text-4xl">Event</h1>
    </div>
    <div class="basis-1/4 my-auto relative py-10 mt-10">
      <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-2 lg:grid-cols-3 gap-4">
          <NuxtLink v-for="(card, index) of cards" :key="index" :to="card.to">
            <div class="flex flex-col bg-white rounded-lg shadow-lg overflow-hidden hover:bg-gray-300">
              <img :src="card.image" class="h-72 bg-gray-400 bg-cover bg-center" />
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