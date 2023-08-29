<script setup lang="ts">
interface Cards {
  title: string;
  image: string;
}

const cards: Cards[] = [
  { title: "Card Title1", image: "https://picsum.photos/seed/picsum/200/300" },
  { title: "Card Title2", image: "https://picsum.photos/seed/picsum/200/300" },
  { title: "Card Title3", image: "https://picsum.photos/seed/picsum/200/300" },
  { title: "Card Title4", image: "https://picsum.photos/seed/picsum/200/300" },
  { title: "Card Title5", image: "https://picsum.photos/seed/picsum/200/300" },
  { title: "Card Title6", image: "https://picsum.photos/seed/picsum/200/300" },
];
</script>

<template>
  <div class="max-w-7xl px-4 sm:px-6 lg:px-8 mx-auto w-full h-full">
    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
      <div class="my-auto relative">
        <div class="flex flex-cols justify-center sm:mt-24">
          <CountDownTimer></CountDownTimer>
        </div>
        <div class="flex justify-center">
          <img
            class="w-full"
            src="~/assets/pic2.png"
            alt="your-image-description"
          />
        </div>
      </div>
      <div class="my-24 sm:ml-20">
        <div
          class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-2 lg:grid-cols-3 gap-4"
        >
          <div
            v-for="(card, index) of cards"
            :key="index"
            class="flex flex-col bg-white rounded-lg shadow-lg overflow-hidden"
          >
            <img
              :src="card.image"
              class="h-48 bg-gray-400 bg-cover bg-center"
            />
            <div class="p-6">
              <h3 class="text-xl font-semibold mb-2">{{ card.title }}</h3>
            </div>
          </div>
        </div>
        <div class="flex flex-row py-0 mt-8 justify-center items-center space-x-5">
          <!-- <div class=""> -->
          <div class="w-40">
            <button class="hover:bg-black hover:text-white bg-white text-center text-lg text-black px-4 py-4 rounded-md border font-bold border-black w-full">
              question
            </button>
          </div>
          <div class="w-40">
            <NuxtLink to="/event">
              <button
                class="hover:bg-black hover:text-white bg-white text-center text-lg text-black px-4 py-4 rounded-md border font-bold border-black w-full"
              >
                event
              </button>
            </NuxtLink>
          </div>
          <!-- </div> -->
        </div>
      </div>
    </div>
  </div>
</template>
