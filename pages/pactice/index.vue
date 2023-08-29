<script setup lang="ts">
const route = useRoute()
const { data } = await useFetch('https://api.nuxtjs.dev/mountains?limit=5', {
    method: 'GET'
})
const page = ref(1)
</script>

<template>
<div class="px-4 sm:px-6 lg:px-8 mx-auto w-full h-full mt-24">
  <div class="flex flex-col text-center w-full mb-0">
    <div class="basis-1/4 my-auto relative py-5">
      <h1 class="font-bold text-5xl">Pactice</h1>
    </div>
    <div class="basis-1/4 my-auto relative py-3">
      <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-5 gap-4">
            <NuxtLink v-for="(card, index) of data" :key="index" to="pactice/1">
                <div class="flex flex-col bg-white rounded-lg shadow-lg overflow-hidden hover:bg-gray-300 transition duration-300 ease-in-out hover:scale-105 cursor-pointer">
                    <img class="h-64 bg-cover bg-center" :src="card.image" />
                    <div class="p-6">
                        <h3 class="text-xl font-semibold mb-2">{{ card.title }}</h3>
                    </div>
                </div>
            </NuxtLink>

            <NuxtLink v-for="(card, index) of data" :key="index" to="pactice/1">
                <div class="flex flex-col bg-white rounded-lg shadow-lg overflow-hidden hover:bg-gray-300 transition duration-300 ease-in-out hover:scale-105 cursor-pointer">
                    <img class="h-64 bg-cover bg-center" :src="card.image" />
                    <div class="p-6">
                        <h3 class="text-xl font-semibold mb-2">{{ card.title }}</h3>
                    </div>
                </div>
            </NuxtLink>
        </div>

        <nav class="flex items-center justify-center mt-10">
          <a href="#" class="block py-3 px-6 text-xl rounded-lg bg-gray-200 hover:bg-gray-300 mr-2">
            Previous
          </a>
          <a href="#" class="block py-3 px-6 text-xl rounded-lg bg-gray-200 hover:bg-gray-300 mr-2">
            1
          </a>
          <a href="#" class="block py-3 px-6 text-xl rounded-lg bg-gray-200 hover:bg-gray-300 mr-2">
            2
          </a>
          <a href="#" class="block py-3 px-6 text-xl rounded-lg bg-gray-200 hover:bg-gray-300 mr-2">
            3
          </a>
          <a href="#" class="block py-3 px-6 text-xl rounded-lg bg-gray-200 hover:bg-gray-300 mr-2">
            Next
          </a>
        </nav>

    </div>
  </div>
</div>
</template>