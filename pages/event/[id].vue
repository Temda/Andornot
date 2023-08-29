<script setup lang="ts">

const route = useRoute()
const id = route.params.id
let text: string
let image: string
if(id === '1'){
  text = 'Halloween'
  image = 'https://www.matichon.co.th/wp-content/uploads/2018/10/Halloween.jpg'
}else if(id === '2'){
  text = 'Christmas'
  image = 'https://images.theconversation.com/files/435160/original/file-20211201-25-puq00f.jpg?ixlib=rb-1.1.0&q=45&auto=format&w=1200&h=900.0&fit=crop'
}else if(id === '3'){
  text = 'Valentine'
  image = 'https://static.nationalgeographic.co.uk/files/styles/image_3200/public/02-valentines-day-reference-595267254.jpg?w=1600&h=900'
}


</script>

<template>
<section>
    <!-- py-24 -->
  <div class="container px-5 mx-auto flex flex-wrap mt-40">
    <div class="lg:w-1/2 w-full mb-10 lg:mb-0 rounded-lg overflow-hidden">
      <img alt="feature" class="object-cover object-center h-5/6 w-full" :src="image">
    </div>
    <div class="flex flex-col flex-wrap lg:py-6 -mb-10 lg:w-1/2 lg:pl-12 lg:text-left text-center">
      <div class="flex flex-col mb-10 lg:items-start items-center">
        <div class="flex-grow mb-10">
          <!-- <h2 class="text-gray-900 text-5xl title-font font-medium mb-3 text-center" v-if="id === '1'">Halloween</h2>
          <h2 class="text-gray-900 text-5xl title-font font-medium mb-3 text-center" v-if="id === '2'">Christmas</h2>
          <h2 class="text-gray-900 text-5xl title-font font-medium mb-3 text-center" v-if="id === '3'">Valentine</h2> -->
          <h2 class="text-gray-900 text-5xl title-font font-medium mb-3 text-center">{{  text }}</h2>


          <p class="leading-relaxed text-base text-center">
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
  </div>
</section>
</template>