<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>
<template>
  <nav class="hidden absolute top-0 left-0 w-full lg:flex justify-between items-center pl-3 lg:pl-16 lg:pt-10 z-50">
    <RouterLink to="/" class="logo">
      <img src="@/assets/images/shared/logo.svg" alt="Company Logo">
    </RouterLink>
    <ul class="flex text-white gap-12  pl-32 pr-16 uppercase backdrop-blur-md bg-white/10">
      <RouterLink to="/" class="border-white border-b-2 py-10"><span class="font-bold pr-2">00</span> HOME</RouterLink>
      <RouterLink to="/destination" class="py-10"><span class="font-bold pr-2">01</span> DESTINATION</RouterLink>
      <RouterLink to="/crew" class="py-10"><span class="font-bold pr-2">02</span> CREW</RouterLink>
      <RouterLink to="/technology" class="py-10"><span class="font-bold pr-2">03</span> TECHNOLOGY</RouterLink>
    </ul>
  </nav>
  <RouterView />
</template>
