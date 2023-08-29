<script setup lang="ts">
// definePageMeta({
//   layout: false
// })
</script>
<template>
<div class="flex flex-row h-screen">
  <div class="flex flex-1 sm:flex-none sm:w-2/3 md:flex-none md:w-full lg:flex-none lg:w-8/12 flex-col bg-slate-50 min-h-screen">
    <div class="flex flex-col h-70 w-9/12 mx-auto items-center my-auto">
    <div class="h-48 w-48 flex items-center justify-center rounded-full bg-gray-200 mt-20">
        <div class="h-full w-full rounded-full overflow-hidden">
            <img class="h-full w-full object-cover" src="https://via.placeholder.com/150" alt="Profile image">
        </div>
    </div>
      <div class="px-2">
        <form class="py-2">
          <div class="flex flex-col py-1">
            <label for="fullname">Fullname</label>
            <span class="mt-2">
                <input class="w-full p-2 mb-6 text-gray-700 border-b-2 border-gray-500 outline-none" type="text" name="fullname" placeholder="Fullname">
            </span>
          </div>
          <div class="flex flex-col py-1">
            <label for="username">Username</label>
            <span class="mt-2">
                <input class="w-full p-2 mb-6 text-gray-700 border-b-2 border-gray-500 outline-none" type="text" name="username" placeholder="Username">
            </span>
          </div>
          <div class="flex flex-col py-1">
            <label for="email">Email</label>
            <span class="mt-2">
                <input class="w-full p-2 mb-6 text-gray-700 border-b-2 border-gray-500 outline-none" type="email" name="email" placeholder="Email">
            </span>
          </div>
          <div class="flex flex-row py-4 space-x-3 justify-center">
            <NuxtLink to="/">
                <button type="button" class="w-32 text-sm sm:w-52 md:w-40 bg-white text-center text-black px-4 py-2 font-bold rounded-md border border-black hover:bg-black hover:text-white">Save Changes</button> 
            </NuxtLink>
            <NuxtLink to="/changepassword">
                <button type="button" class="w-32 text-sm sm:w-52 md:w-40 bg-white text-center text-black px-4 py-2 font-bold rounded-md border border-black hover:bg-black hover:text-white">Change Password</button>
            </NuxtLink>
        </div>
        </form>
      </div>
    </div>
  </div>
  <div class="hidden justify-center items-center flex-1 lg:flex bg-cover bg-black">
    <!-- <div class="w-"> -->
      <img src="~/assets/pic3.png" class="w-96 object-contain">
    <!-- </div> -->
  </div>
</div>
</template>