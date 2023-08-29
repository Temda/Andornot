<script setup lang="ts">
const Manubars = ref(false)
function Manubar() {
  Manubars.value = !Manubars.value;
}
interface Nav {
  name: string;
  to: string;
}
const navbar: Nav[] = [
  {name: 'home', to: '/'},
  {name: 'event', to: '/event'},
  {name: 'question', to: '/question'},
  {name: 'pactice', to: '/pactice'},
  {name: 'ranking', to: '/ranking'}

]

</script>

<template>
  <div class="min-h-screen">
    <div class="flex flex-col min-h-screen justify-between">
    <nav class="bg-neutral-200 border-gray-200 px-2 sm:px-4 py-2.5 w-full z-50 shadow-lg absolute">
      <!-- <div class="bg-red-800 w-full h-1"></div> -->
      <div class="container flex flex-wrap items-center justify-between mx-auto">
        <NuxtLink to="/" class="flex items-center">
          <img src="~/assets/logo.png" class="h-10 mr-3 sm:h-10" alt="Flowbite Logo"
          />
          <span
            class="self-center text-3xl font-semibold whitespace-nowraptext-black"
            >Andornot</span
          >
        </NuxtLink>
        <button
          @click="Manubar"
          data-collapse-toggle="navbar-default"
          type="button"
          class="inline-flex items-center p-2 ml-3 text-sm text-gray-500 rounded-lg md:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600"
          aria-controls="navbar-default"
          aria-expanded="false"
        >
          <span class="sr-only">Open main menu</span>
          <svg
            class="w-6 h-6"
            aria-hidden="true"
            fill="currentColor"
            viewBox="0 0 20 20"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              fill-rule="evenodd"
              d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 15a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z"
              clip-rule="evenodd"
            ></path>
          </svg>
        </button>
        <div :class="[!Manubars ? 'hidden' : '']" class="w-full md:block md:w-auto" id="navbar-default">
          <ul
            class="flex flex-col p-4 mt-4 border border-gray-100 rounded-lg bg-gray-50 md:flex-row md:space-x-8 md:mt-0 md:text-sm md:font-medium md:border-0 bg-neutral-200">
            <li
            v-for="(navbas, index) in navbar"
            :key="index">
              <NuxtLink
                :to="navbas.to"
                class="block py-2 pl-3 pr-4 text-black text-2xl rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:p-0 hover:text-white"
                aria-current="page"
                >{{ navbas.name }}</NuxtLink>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    
    <main class="mb-auto">
              <slot />

      <!-- </section> -->
    </main>

    <!-- <footer class="bg-gray-100 py-6 px-2">
        <div class="flex justify-center items-center"> 
                Copyright 2023
        </div>
    </footer> -->
  </div>
</div>
</template>