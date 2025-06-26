<template>
  <div id="card" class="bg-white w-[290px] h-[378px] m-2">
    <div id="gambar" class="bg-gray-100">
      <img :src="gambar" alt="gambar5" class="object-cover w-72 h-80 p-4" />

      <div class="flex justify-center py-5 space-x-2">
        <Cart class="text-orange-600" />
        <h1 class="text-orange-600">Add cart</h1>
      </div>
    </div>
    <div id="title" class="mt-6">
      <h1 class="text-gray-800 text-xl">{{ props.title }}</h1>
      <h1 class="font-medium text-lg">${{ props.harga }}</h1>
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
