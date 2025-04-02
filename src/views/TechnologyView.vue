<script setup>
import { onMounted, ref } from "vue";

const tabsActive = ref(null);
const tabs = ref([
  {
    id: 1, supTitle: 'THE TERMINOLOGY…',
    title: 'LAUNCH VEHICLE',
    content: "A launch vehicle or carrier rocket is a rocket-propelled vehicle used to carry a payload from Earth's surface to space, usually to Earth orbit or beyond. Our WEB-X carrier rocket is the most powerful in operation. Standing 150 metres tall, it's quite an awe-inspiring sight on the launch pad!",
    imgUrl: '/images/technology/image-launch-vehicle-portrait.jpg',
    imgUrlMob: '/images/technology/image-launch-vehicle-landscape.jpg'
  },
  {
    id: 2, supTitle: 'THE TERMINOLOGY…',
    title: 'SPACEPORT',
    content: "A spaceport or cosmodrome is a site for launching (or receiving) spacecraft, by analogy to the seaport for ships or airport for aircraft. Based in the famous Cape Canaveral, our spaceport is ideally situated to take advantage of the Earth’s rotation for launch.",
    imgUrl: '/images/technology/image-spaceport-portrait.jpg',
    imgUrlMob: '/images/technology/image-spaceport-landscape.jpg'
  },
  {
    id: 3, supTitle: 'THE TERMINOLOGY…',
    title: 'SPACE CAPSULE',
    content: "A space capsule is an often-crewed spacecraft that uses a blunt-body reentry capsule to reenter the Earth's atmosphere without wings. Our capsule is where you'll spend your time during the flight. It includes a space gym, cinema, and plenty of other activities to keep you entertained.",
    imgUrl: '/images/technology/image-space-capsule-portrait.jpg',
    imgUrlMob: '/images/technology/image-space-capsule-landscape.jpg'

  },

]);

onMounted(() => {
  tabsActive.value = tabs.value[0]
})

</script>
<template>
  <main
    class="h-max-screen bg-[url(@/assets/images/technology/background-technology-mobile.jpg)] md:bg-[url(@/assets/images/technology/background-technology-tablet.jpg)] lg:bg-[url(@/assets/images/technology/background-technology-desktop.jpg)] bg-no-repeat bg-cover bg-blue-900">
    <div class="flex items-center justify-center min-h-screen lg:overflow-hidden pt-20 lg:pt-40">
      <div class="container lg:max-w-lg text-center lg:text-left text-white">
        <h2
          class="my-6 md:text-left text-mobile-preset-6 md:text-tablet-preset-5 lg:text-desctop-preset-5 font-tertiary tracking-[4px]">
          <span class="mr-6 text-white/50 font-tertiary font-bold tracking-[2.7px]">03</span>
          SPACE LAUNCH 101
        </h2>
        <div class="grid lg:grid-cols-2 lg:px-0 gap-8 justify-between">
          <div class="my-8 gap-8 flex flex-col lg:flex-row items-center order-2 lg:order-1">
            <div class="flex flex-row lg:flex-col items-center gap-8">
              <button v-for="tab in tabs" :key="tab.id" @click="tabsActive = tab"
                class="cursor-pointer w-10 h-10 md:w-14 md:h-14 lg:w-20 lg:h-20 rounded-full border text-mobile-preset-4 md:text-tablet-preset-4 lg:text-desctop-preset-4"
                :class="tabsActive?.id === tab.id ? 'bg-white text-black' : ''">
                {{  tab?.id }}</button>
            </div>
            <div class="md:px-16 lg:px-0">
              <h2 class="text-mobile-preset-4 md:text-tablet-preset-4 lg:text-desctop-preset-4 uppercase text-white/50">
                {{ tabsActive?.supTitle }}</h2>
              <h1
                class="text-mobile-preset-3 md:text-tablet-preset-3 lg:text-desctop-preset-3 uppercase whitespace-nowrap">
                {{ tabsActive?.title }}</h1>
              <p
                class="text-mobile-preset-9 md:text-tablet-preset-9 lg:text-desctop-preset-9  leading-[180%] text-blue-300 my-6 font-secondary font-normal">
                {{ tabsActive?.content }}
              </p>
            </div>
          </div>
          <div class="flex justify-end relative order-1 lg:order-2 lg:hidden">
            <img class="z-10 md:w-full lg:absolute lg:left-14 lg:-top-10"  :src="tabsActive?.imgUrlMob" alt="Moon">
          </div>
          <div class="hidden lg:flex lg:justify-end lg:relative order-1 lg:lg:order-2">
            <img class="z-10 md:w-full lg:absolute lg:left-14 lg:-top-10"  :src="tabsActive?.imgUrl" alt="Moon">
          </div>
        </div>
      </div>
    </div>
  </main>
</template>
