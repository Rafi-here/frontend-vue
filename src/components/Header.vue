<template>
  <div class="border-b border-gray-200 shadow flex z-50 justify-between items-center py-4 md:py-[27px] px-6 sm:px-12 lg:px-24 bg-white">
    <!-- Logo -->
    <div id="logo" class="w-32 md:w-auto">
      <a href="#sectionHero">
        <img :src="logoHeader" alt="Company logo with modern design" class="w-full h-auto" />
      </a>
    </div>

    <!-- Desktop Menu (hidden on mobile) -->
    <div id="menu-desktop" class="hidden md:flex space-x-8 lg:space-x-14">
      <h1 class="text-base lg:text-xl"><a href="#card">Product</a></h1>
      <h1 class="text-base lg:text-xl"><a href="#services">Services</a></h1>
      <h1 class="text-base lg:text-xl"><a href="#gallery">Article</a></h1>
      <h1 class="text-base lg:text-xl"><a href="#about">About Us</a></h1>
    </div>

    <div id="user" class="flex space-x-4">
      <Cart class="text-black w-6 h-6" />
      <User class="w-6 h-6" />
    </div>

    <!-- Mobile Menu Button -->
    <button @click="toggleMenu" class="md:hidden text-black">
      <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
      </svg>
    </button>

    <!-- Mobile Menu (dropdown) -->
    <div v-if="isMenuOpen" class="md:hidden absolute top-20 left-0 right-0 bg-white shadow-lg py-3 px-6 z-40">
      <h1 class="text-base py-2 border-b border-gray-100"><a href="#card" @click="toggleMenu">Product</a></h1>
      <h1 class="text-base py-2 border-b border-gray-100"><a href="#services" @click="toggleMenu">Services</a></h1>
      <h1 class="text-base py-2 border-b border-gray-100"><a href="#gallery" @click="toggleMenu">Article</a></h1>
      <h1 class="text-base py-2"><a href="#about" @click="toggleMenu">About Us</a></h1>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import { logoHeader } from '@/assets/image';
import { Cart, User } from './icons';

const isMenuOpen = ref(false);

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};
</script>
