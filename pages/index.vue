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
      <!-- <div class="container mx-auto py-8"> -->
      <div class="flex flex-col md:flex-row justify-center mt-20">
        <div class="md:w-3/4">

          <section id="section1" class="mb-8">
            <div class="flex flex-col text-center w-full mb-20">
              <div class="grid grid-cols-1 sm:grid-cols-2 gap-1 sm:mt-10 lg:mt-20 xl:mt-10">
                <div class="my-auto relative">
                  <div class="text-right">
                      <div class="flex justify-center">
                          <img class="w-full" src="~/assets/pic1.png" alt="your-image-description">
                      </div>
                  </div>
                </div>
                <div class="flex flex-col justify-center items-center">
                  <div class="flex flex-cols">
                    <CountDownTimer></CountDownTimer>
                  </div>
                  <div class="space-x-4">
                    <NuxtLink to="/">
                      <button class="bg-white text-center text-black px-4 py-3 rounded-md border border-black hover:text-white hover:bg-black">Join Now</button>
                    </NuxtLink>
                    <NuxtLink to="/login">
                      <button class="bg-white text-center text-black px-4 py-3 rounded-md border border-black hover:text-white hover:bg-black">Login</button>
                    </NuxtLink>
                  </div>
                </div>
              </div>
            </div>
          </section>
    
          <section id="section2" class="mb-8">
            <div class="max-w-7xl px-4 sm:px-6 lg:px-8 mx-auto w-full h-full">
              <div class="flex flex-col text-center w-full mb-20">
                <h2 class="text-4xl font-bold tracking-tight text-center">What is Andornot?</h2>
                <p class="mt-2 text-lg text-center text-gray-600">
                  orem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
                  orem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
                </p>
              </div>
              <div class="flex flex-col text-center w-full mb-20">
                <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-2 lg:grid-cols-3 gap-4">
                  <div
                    v-for="(card, index) of cards"
                    :key="index"
                    class="flex flex-col bg-white rounded-lg shadow-lg overflow-hidden"
                  >
                      <!-- :src="card.image" -->
                    <div class="h-48 bg-gray-400 bg-cover bg-center"></div>
                    <div class="p-6">
                      <h3 class="text-xl font-semibold mb-2">{{ card.title }}</h3>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </section>
<!--     
          <section id="section3" class="mb-8">
            <div class="max-w-7xl px-4 sm:px-6 lg:px-8 mx-auto w-full h-full">
              <div class="flex flex-col text-center w-full mb-20">
                <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-2 lg:grid-cols-3 gap-4">
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
              </div>
            </div>
          </section> -->
          
        </div>
      </div>
    <!-- </div> -->
</template>
    