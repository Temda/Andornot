<script setup lang="ts">

const route = useRoute()
const id = route.params.id
let text: string = 'HALO x74'
let image: string = 'https://static.nationalgeographic.co.uk/files/styles/image_3200/public/02-valentines-day-reference-595267254.jpg?w=1600&h=900'


</script>

<template>
<section>
    <!-- py-24 -->
  <div class="container px-5 mx-auto flex flex-wrap mt-20 lg:mt-40 md:mt-28">
    <div class="flex flex-col flex-wrap lg:py-6 -mb-10 lg:w-1/2 lg:pl-12 lg:text-left text-center">
      <div class="flex flex-col mb-10 lg:items-start items-center">
        <div class="flex-grow mb-10">

          <h2 class="text-gray-900 text-5xl title-font font-medium mb-3 text-center">{{  text }}</h2>


          <p class="leading-relaxed text-base text-center lg:mr-10">
            orem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Nam maxime maiores debitis laudantium rem. Cupiditate dolorem, recusandae et perspiciatis porro reiciendis est placeat quidem magnam! Consectetur distinctio cupiditate debitis quisquam?
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Nam maxime maiores debitis laudantium rem. Cupiditate dolorem, recusandae et perspiciatis porro reiciendis est placeat quidem magnam! Consectetur distinctio cupiditate debitis quisquam?
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Nam maxime maiores debitis laudantium rem. Cupiditate dolorem, recusandae et perspiciatis porro reiciendis est placeat quidem magnam! Consectetur distinctio cupiditate debitis quisquam?
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Nam maxime maiores debitis laudantium rem. Cupiditate dolorem, recusandae et perspiciatis porro reiciendis est placeat quidem magnam! Consectetur distinctio cupiditate debitis quisquam?
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Nam maxime maiores debitis laudantium rem. Cupiditate dolorem, recusandae et perspiciatis porro reiciendis est placeat quidem magnam! Consectetur distinctio cupiditate debitis quisquam?
          </p>

        </div>
      </div>
    </div>
    <div class="lg:w-1/2 w-full mb-10 lg:mb-0 rounded-lg overflow-hidden">
      <img alt="feature" class="object-cover object-center h-4/5 w-full" :src="image">
      <!-- <div class="flex flex-col w-4/6  flex-wrap mt-5">
        <input type="text" id="text" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5" placeholder="Your Answer" required>
      </div> -->
      <div class="flex flex-row mt-20 space-x-3 mb-20">
        <div class="basis-full">
          <input type="text" id="text" class="bg-white border border-gray-500 text-gray-900 text-lg rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5" placeholder="Your Answer" required>
        </div>
        <div class="basis-44">
          <button type="submit" class="text-white bg-black hover:bg-white hover:text-black border border-gray-900 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm w-full sm:w-auto px-10 py-3.5 text-center">Submit</button>
        </div>
      </div>
      
    </div>
  </div>
</section>
</template>