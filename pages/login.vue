<script setup lang="ts">
// definePageMeta({
//   layout: false
// })
</script>
<template>
<div class="flex flex-row h-screen">
  <div class="hidden justify-center items-center flex-1 lg:flex bg-cover bg-black">
    <!-- <div class="w-"> -->
      <img src="~/assets/pic3.png" class="w-96 object-contain">
    <!-- </div> -->
  </div>
  <div class="flex flex-1 sm:flex-none sm:w-2/3 md:flex-none md:w-full lg:flex-none lg:w-8/12 flex-col bg-slate-50 min-h-screen">
    <div class="flex flex-col h-70 w-9/12 mx-auto items-center my-auto">
      <div class="px-2">
        <h1 class="text-4xl font-bold my-1 text-center">Login</h1>
        <form class="py-2">
          <div class="flex flex-col py-1">
            <label for="email">Email</label>
            <span class="mt-2">
                <input class="w-full p-2 mb-6 text-gray-700 border-b-2 border-gray-500 outline-none" type="email" name="email" placeholder="Email">
            </span>
          </div>
          <div class="flex flex-col py-1">
            <label for="password">Password</label>
            <span class="mt-2">
                <input class="w-full p-2 mb-6 text-gray-700 border-b-2 border-gray-500 outline-none" type="password" name="password" placeholder="password">
            </span>
          </div>
          <div class="flex flex-row py-2">
            <span class="flex flex-1 flex-row-reverse">
              <a href="/forget-password" class="text-taltech-blue text-md underline">Forget password</a>
            </span>
          </div>
          <div class="flex flex-row py-4 space-x-3 justify-center">
            <NuxtLink to="">
                <button type="submit" class="w-32 sm:w-52 md:w-40 bg-white text-center text-black px-4 py-2 font-bold rounded-md border border-black hover:bg-green-600 hover:border-green-500 hover:text-white">Login</button> 
            </NuxtLink>
            <NuxtLink to="/register">
                <button type="button" class="w-32 sm:w-52 md:w-40 bg-white text-center text-black px-4 py-2 font-bold rounded-md border border-black hover:bg-black hover:text-white">Register</button>
            </NuxtLink>
        </div>
        </form>
      </div>
    </div>
  </div>
</div>
</template>