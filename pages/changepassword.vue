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
    <div class="h-48 w-48 flex items-center justify-center rounded-full bg-gray-200 mt-20">
        <div class="h-full w-full rounded-full overflow-hidden">
            <img class="h-full w-full object-cover" src="https://via.placeholder.com/150" alt="Profile image">
        </div>
    </div>
      <div class="px-2">
        <form class="py-2">
          <div class="flex flex-col py-1 w-96">
            <label for="fullname">Old Password</label>
            <span class="mt-2">
                <input class="w-full p-2 mb-6 text-gray-700 border-b-2 border-gray-500 outline-none" type="password" name="oldpassword" placeholder="******">
            </span>
          </div>
          <div class="flex flex-col py-1 w-96">
            <label for="username">New Password</label>
            <span class="mt-2">
                <input class="w-full p-2 mb-6 text-gray-700 border-b-2 border-gray-500 outline-none" type="password" name="newpassword" placeholder="******">
            </span>
          </div>
          <div class="flex flex-col py-1 w-96">
            <label for="email">Confirm Password</label>
            <span class="mt-2">
                <input class="w-full p-2 mb-6 text-gray-700 border-b-2 border-gray-500 outline-none" type="password" name="confirmpassword" placeholder="******">
            </span>
          </div>
          <div class="flex flex-row py-4 space-x-3 justify-left">
            <NuxtLink to="/">
                <button type="button" class="w-32 text-sm sm:w-52 md:w-40 bg-white text-center text-black px-4 py-2 font-bold rounded-md border border-black hover:bg-black hover:text-white">Save Changes</button> 
            </NuxtLink>
        </div>
        </form>
      </div>
    </div>
  </div>
</div>
</template>