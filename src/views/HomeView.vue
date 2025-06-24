<script setup>
import { IconKacamataPembesar } from '@/components/icons'
import { g1, g2, g3, g4 } from '@/assets/image'

const images = [g1, g2, g3, g4, g1, g2]
</script>

<template>
  <section id="sectionHero" class="space-y-20">
    <div class="space-y-[27px]">
      <h1 class="text-7xl text-black font-medium text-center mt-60 mx-60">
        Transform your space, Elevate your style.
      </h1>
      <h2 class="text-xl text-center mx-60">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Ex error veritatis tempore quae
        magni in temporibus, maiores vel. Nobis, dolore quod. Excepturi, molestiae aliquam vel
        explicabo laborum autem velit nesciunt!
      </h2>
    </div>

    <div class="flex justify-center w-full">
      <div class="flex justify-center w-[667px] py-4 pr-4 pl-6 bg-gray-200">
        <IconKacamataPembesar class="m-4" />
        <input
          class="bg-gray-200 outline-none border border-gray-200 w-full"
          placeholder="Search your property"
        />
        <button class="bg-orange-600 p-3 text-white">Search</button>
      </div>
    </div>

    <!-- gambar -->
    <div class="flex space-x-10">
      <div class="overflow-x-auto" v-for="gambar in images">
        <img :src="gambar" alt="gambar1" class="object-cover h-80 w-80" />
      </div>
    </div>
  </section>
</template>
