<script>
export default {
  name: "FurnitureReview",
  props: ["human", "kursi"],
};
</script>

<template>
  <div class="relative w-full overflow-hidden">
    <div class="absolute top-0 left-0 w-full h-1/2 bg-gray-100 z-0"></div>
    <div class="absolute top-1/2 left-0 w-full h-1/2 bg-orange-400 z-0"></div>

    <div class="relative z-10 max-w-8xl  px-6 py-12 grid md:grid-cols-2 gap-8 items-center">
      <div class="space-y-6">
        <div class="flex items-center gap-3">
          <img :src="human" alt="User" class="w-12 h-12 rounded-full" />
          <div>
            <h4 class="text-lg font-semibold text-gray-800">Kim Shan Dhi</h4>
            <p class="text-sm text-gray-500">Director Google Inc.</p>
          </div>
        </div>

        <p class="text-gray-600 text-base leading-relaxed">
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Consequatur, 
          voluptates. Facere perferendis nam ipsa ab molestiae facilis. Possimus molestiae 
          temporibus, accusamus rerum corrupti dolorem provident obcaecati nihil, laborum inventore quasi.
        </p>

        <div class="flex gap-1 text-yellow-400 text-lg">
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star text-gray-300"></i>
        </div>
<div class="text-left">
    <img :src="kursi" alt="kursi" class="flex w-400 h-100" />

    <p class="text-4xl text-white font-medium mt-8">Subscribe to get attractive offers on our products</p>
        </div>
        </div>

        <div class="flex flex-col justify-center items-center text-center mb-30">
        <span class="bg-indigo-100 text-indigo-600 text-m font-semibold px-3 py-1 rounded">Review</span>
        <h2 class="text-4xl font-bold text-gray-800 mt-2">Our Furniture Review</h2>
        <p class="text-gray-600 mt-3 leading-relaxed text-base max-w-md">
          Lorem Ipsum is simply dummy text of the printing and typesetting industry.
        </p>

        <div class="bg-white rounded-lg p-2 flex mt-50 shadow-lg w-full max-w-md">
          <input
            type="email"
            placeholder="E.g. youremail@mail.com"
            class="flex-1 px-4 py-2 rounded-l-md focus:outline-none text-gray-800"
          />
          <button class="bg-blue-700 hover:bg-blue-500 text-white px-6 py-2 rounded-md">
            Subscribe
          </button>
        </div>
      </div>
    </div>

    <div class="absolute top-4 left-1/2 translate-x-1/2 flex gap-4">
      <button
        class="bg-white border border-gray-300 hover:bg-gray-100 rounded-full w-8 h-8 flex items-center justify-center shadow">
        <i class="fas fa-chevron-left text-sm text-gray-600"></i>
      </button>
      <button
        class="bg-white border border-gray-300 hover:bg-gray-100 rounded-full w-8 h-8 flex items-center justify-center shadow">
        <i class="fas fa-chevron-right text-sm text-gray-600"></i>
      </button>
    </div>
  </div>
</template>
