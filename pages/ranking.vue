<script setup lang="ts">
interface Scores {
    rating: number;
    name: string;
}
const data = [
    {rating: 1, name: 'John1 Doe'},
    {rating: 2, name: 'John2 Doe'},
    {rating: 3, name: 'John3 Doe'},
    {rating: 4, name: 'John4 Doe'},
    {rating: 5, name: 'John5 Doe'},
    {rating: 6, name: 'John6 Doe'},
    {rating: 7, name: 'John7 Doe'},
    {rating: 8, name: 'John8 Doe'},
    {rating: 9, name: 'John9 Doe'},
    {rating: 10, name: 'John10 Doe'}
]

const activeTab = ref('tab1')

const isActive = ref(false)
function toggleActive() {
      isActive.value = !isActive.value;
}
</script>
<template>
  <div class="flex flex-col md:flex-row justify-center mt-20">
    <div class="md:w-3/4">
      <section id="section1" class="mb-8">
        <div class="flex flex-col text-center w-full mb-20">
          <div
            class="grid grid-cols-1 sm:grid-cols-2 gap-1 sm:mt-10 lg:mt-20 xl:mt-10"
          >
            <div class="my-auto relative">
              <div class="text-center mt-10">
                <h2 class="text-4xl font-bold tracking-tight">
                  -- You are the 1ST --
                </h2>
                <div class="flex justify-center">
                  <img
                    class="w-full hidden sm:block"
                    src="~/assets/pic1.png"
                    alt="your-image-description"
                  />
                </div>
              </div>
            </div>
            <div class="my-auto relative">
              <div class="text-center">
                <div class="space-x-2">
                    <button
                    @click="activeTab = 'tab1'"
                      type="button"
                      :class="{ 'bg-black text-white': activeTab === 'tab1' }"
                      class="w-40 text-center px-4 py-3 rounded-md border border-black"
                    >
                      Free
                    </button>
                    <button
                      @click="activeTab = 'tab2'"
                      type="button"
                      :class="{ 'bg-black text-white': activeTab === 'tab2' }"
                      class="w-40 text-center px-4 py-3 rounded-md border border-black"
                    >
                      Noob
                    </button>
                </div>

                <div class="flex justify-center" v-if="activeTab === 'tab1'">
                  <table class="table-auto w-96">
                    <thead>
                      <tr>
                        <th class="px-4 py-2">Number</th>
                        <th class="px-4 py-2">Name</th>
                      </tr>
                    </thead>
                    <tbody>
                      <tr v-for="(datas, index) of data" :key="index">
                        <td class="border px-4 py-2">{{ datas.rating }}</td>
                        <td class="border px-4 py-2">{{ datas.name }}</td>
                      </tr>
                    </tbody>
                  </table>
                </div>

                <div class="flex justify-center" v-if="activeTab === 'tab2'">
                  <table class="table-auto w-96">
                    <thead>
                      <tr>
                        <th class="px-4 py-2">Number</th>
                        <th class="px-4 py-2">Name</th>
                      </tr>
                    </thead>
                    <tbody>
                      <tr v-for="(datas, index) of data" :key="index">
                        <td class="border px-4 py-2">{{ datas.rating }}</td>
                        <td class="border px-4 py-2">{{ datas.name }}</td>
                      </tr>
                    </tbody>
                  </table>
                </div>

              </div>
            </div>
          </div>
        </div>
      </section>
    </div>
  </div>
</template>
