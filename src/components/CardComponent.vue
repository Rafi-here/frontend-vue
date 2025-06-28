<template>
  <div id="card" class="relative bg-white w-[290px] h-[378px] m-2 mb-10 shadow rounded-lg overflow-hidden">
    <!-- Label Diskon -->
    <div class="absolute top-2 left-2 bg-red-500 text-white text-xs font-semibold px-2 py-1 rounded z-10 shadow">
      -35%
    </div>

    <!-- Gambar -->
    <div id="gambar" class="bg-gray-100">
      <img :src="gambar" alt="gambar produk" class="object-cover w-full h-60 p-2" />

      <!-- Tombol Cart -->
      <div class="flex justify-center py-5 space-x-2">
        <Cart class="text-orange-600" />
        <h1 class="text-orange-600 font-medium">Add cart</h1>
      </div>
    </div>

    <!-- Judul & Harga -->
    <div id="title" class="px-4 mt-2">
      <h1 class="text-gray-800 text-lg font-semibold truncate">{{ props.title }}</h1>
      <h1 class="font-medium text-base text-green-600">${{ props.harga }}</h1>
    </div>
  </div>

</template>

<script setup>
import { Cart } from './icons'

const props = defineProps({
  title: {
    type: String,
    required: true,
  },
  harga: {
    type: Number,
    required: true,
  },
  gambar: {
    type: String,
    required: true,
  },
})
</script>
