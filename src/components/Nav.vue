<script setup>
import { RouterLink, RouterView, useRoute } from 'vue-router'
import { ref } from 'vue'

const route = useRoute()
const isMenuOpen = ref(false)

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}
</script>

<template>
  <nav class="absolute top-0 left-0 w-full flex justify-between lg:items-center pl-3 lg:pl-16 lg:pt-10 z-50 font-tertiary tracking-[2px]">
    <RouterLink to="/" class="cursor-pointer logo mt-6 lg:mt-0">
      <img src="@/assets/images/shared/logo.svg" alt="Company Logo">
    </RouterLink>

    <!-- Гамбургер кнопка (видна только на мобильных) -->
    <button
      class="cursor-pointer mt-9 pr-6 flex items-center justify-end lg:hidden z-50"
      @click="toggleMenu"
      v-if="!isMenuOpen"
    >
      <img class="cursor-pointer" src="@/assets/images/shared/icon-hamburger.svg" alt="icon-hamburger">
    </button>

    <!-- Меню (с анимацией и состоянием) -->
    <div
      class="h-screen lg:h-auto fixed lg:relative top-0 right-0 flex flex-col lg:flex-row w-[254px] lg:w-7/12 text-white pl-6 lg:pt-0 lg:gap-12 lg:pl-32 lg:pr-16 uppercase backdrop-blur-md bg-white/10 transition-transform duration-300 ease-in-out"
      :class="{
        'translate-x-0': isMenuOpen,
        'translate-x-full lg:translate-x-0': !isMenuOpen
      }"
    >
      <!-- Кнопка закрытия (видна только на мобильных) -->
      <button
        class="cursor-pointer mb-12 mt-9 pr-6 flex items-center justify-end lg:hidden"
        @click="toggleMenu"
        v-if="isMenuOpen"
      >
        <img class="cursor-pointer" src="@/assets/images/shared/icon-close.svg" alt="icon-close">
      </button>

      <!-- Ссылки меню -->
      <RouterLink
        to="/"
        class="text-desctop-preset-7 border-r-3 lg:border-r-0 lg:border-b-3 mb-8 lg:mb-0 lg:py-10"
        :class="{
          'border-white': route.path === '/',
          'border-transparent': route.path !== '/'
        }"
        @click="isMenuOpen = false"
      >
        <span class="font-bold pr-2">00</span> HOME
      </RouterLink>

      <RouterLink
        to="/destination"
        class="text-desctop-preset-7 border-r-3 lg:border-r-0 lg:border-b-3 mb-8 lg:mb-0 lg:py-10"
        :class="{
          'border-white': route.path === '/destination',
          'border-transparent': route.path !== '/destination'
        }"
        @click="isMenuOpen = false"
      >
        <span class="font-bold pr-2">01</span> DESTINATION
      </RouterLink>

      <RouterLink
        to="/crew"
        class="text-desctop-preset-7 border-r-3 lg:border-r-0 lg:border-b-3 mb-8 lg:mb-0 lg:py-10"
        :class="{
          'border-white': route.path === '/crew',
          'border-transparent': route.path !== '/crew'
        }"
        @click="isMenuOpen = false"
      >
        <span class="font-bold pr-2">02</span> CREW
      </RouterLink>

      <RouterLink
        to="/technology"
        class="text-desctop-preset-7 border-r-3 lg:border-r-0 lg:border-b-3 mb-8 lg:mb-0 lg:py-10"
        :class="{
          'border-white': route.path === '/technology',
          'border-transparent': route.path !== '/technology'
        }"
        @click="isMenuOpen = false"
      >
        <span class="font-bold pr-2">03</span> TECHNOLOGY
      </RouterLink>
    </div>
  </nav>

  <RouterView />
</template>
