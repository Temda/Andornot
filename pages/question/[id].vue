<script setup lang="ts">
const route = useRoute()
const { data } = await useFetch('https://api.nuxtjs.dev/mountains', {
    method: 'GET'
})
</script>

<template>
<div class="px-4 sm:px-6 lg:px-8 mx-auto w-full h-full mt-20">
  <div class="flex flex-col text-center w-full mb-20">
    <div class="basis-1/4 my-auto relative py-10 mt-10">
      <h1 class="font-bold text-4xl">Question{{ route.params.id }}</h1>
    </div>
    <div class="basis-1/4 my-auto relative py-5">
      <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-5 gap-4">
          <!-- <NuxtLink v-for="(card, index) of data" :key="index"> -->
            <div v-for="(card, index) of data" :key="index" class="flex flex-col bg-white rounded-lg shadow-lg overflow-hidden hover:bg-gray-300 transition duration-300 ease-in-out hover:scale-105 cursor-pointer">
            <img class="h-64 bg-cover bg-center" :src="card.image" />
              <div class="p-6">
                <h3 class="text-xl font-semibold mb-2">{{ card.title }}</h3>
                <p class="text-sm font-semibold mb-2">{{ card.description }}</p>
              </div>
            </div>
          <!-- </NuxtLink> -->
        </div>
    </div>
  </div>
</div>
</template>