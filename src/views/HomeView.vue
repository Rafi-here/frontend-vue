<script setup>
import { IconKacamataPembesar } from '@/components/icons'
import { g1, g2, g3, g4, g5, logo1, logo2, logo3, logo4, logo5 } from '@/assets/image'
import { CardComponent } from '@/components'

const images = [g1, g2, g3, g4, g1, g2]
const logos = [logo1, logo2, logo3, logo4, logo5]

const barang = [
  {
    title: 'LifeStyle Green Chair',
    harga: 105.0,
    gambar: g1,
  },
  {
    title: 'LifeStyle Cupboard',
    harga: 185.0,
    gambar: g2,
  },
  {
    title: 'LifeStyle Desk',
    harga: 205.0,
    gambar: g3,
  },
  {
    title: 'LifeStyle Green Chair',
    harga: 105.0,
    gambar: g4,
  },
  {
    title: 'LifeStyle Cupboard',
    harga: 185.0,
    gambar: g5,
  },
  {
    title: 'LifeStyle Desk',
    harga: 205.0,
    gambar: g1,
  },
]
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

    <div class="flex justify-between">
      <div class="mx-4" v-for="logo in logos">
        <img :src="logo" alt="logo" class="object-cover" />
      </div>
    </div>
  </section>

  <section id="card" class="my-20 w-full">
    <div class="w-full grid grid-cols-3 gap-20">
      <CardComponent
        v-for="product in barang"
        :key="index"
        :title="product.title"
        :harga="product.harga"
        :gambar="product.gambar"
      />
    </div>
  </section>
</template>
