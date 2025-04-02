<script setup>
import { onMounted, ref } from "vue";

const tabsActive = ref(null);
const tabs = ref([
  {
    id: 1, title: 'MOON',
    content: 'See our planet as you’ve never seen it before. A perfect relaxing trip away to help regain perspective and come back refreshed. While you’re there, take in some history by visiting the Luna 2 and Apollo 11 landing sites.',
    distance: '384,400 km',
    travelTime: '3 days',
    imgUrl: '/images/destination/image-moon.png'
  },
  {
    id: 2, title: 'MARS',
    content: 'Don’t forget to pack your hiking boots. You’ll need them to tackle Olympus Mons, the tallest planetary mountain in our solar system. It’s two and a half times the size of Everest!',
    distance: '225 MIL. km',
    travelTime: '9 months',
    imgUrl: '/images/destination/image-mars.png'
  },
  {
    id: 3, title: 'EUROPA',
    content: 'The smallest of the four Galilean moons orbiting Jupiter, Europa is a winter lover’s dream. With an icy surface, it’s perfect for a bit of ice skating, curling, hockey, or simple relaxation in your snug wintery cabin.',
    distance: '628 MIL. km',
    travelTime: '3 years',
    imgUrl: '/images/destination/image-europa.png'
  },
  {
    id: 4, title: 'TITAN',
    content: 'The only moon known to have a dense atmosphere other than Earth, Titan is a home away from home (just a few hundred degrees colder!). As a bonus, you get striking views of the Rings of Saturn.',
    distance: '1.6 BIL. km',
    travelTime: '7 years',
    imgUrl: '/images/destination/image-titan.png'
  },
]);

onMounted(() => {
  tabsActive.value = tabs.value[0]
})

</script>

<template>
  <main
    class="h-max-screen bg-[url(@/assets/images/destination/background-destination-mobile.jpg)] md:bg-[url(@/assets/images/destination/background-destination-tablet.jpg)] lg:bg-[url(@/assets/images/destination/background-destination-desktop.jpg)] bg-no-repeat bg-cover bg-blue-900">
    <div class="flex items-center justify-center min-h-screen pt-20 lg:pt-40">
      <div class="container lg:max-w-lg text-center md:text-left text-white">
        <h2 class="my-6 text-mobile-preset-6 md:text-tablet-preset-5 lg:text-desctop-preset-5 font-tertiary tracking-[4px]">
          <span class="mr-6 text-white/50 font-tertiary font-bold tracking-[2.7px]">01</span>PICK YOUR DESTINATION
        </h2>
        <div class="grid lg:grid-cols-2 md:px-16 lg:px-0 gap-8 justify-between">
          <div class="flex justify-start relative">
            <img class="z-10 mx-auto w-[228px] md:w-[458px] lg:w-auto " :src="tabsActive?.imgUrl" alt="Moon">
          </div>
          <div class="text-center lg:text-left">
            <div class="flex justify-center lg:justify-start items-center gap-8">
              <button v-for="tab in tabs" :key="tab.id" @click="tabsActive = tab"
                class="cursor-pointer text-blue-300 pb-2 text-mobile-preset-8 md:text-desctop-preset-8"
                :class="tabsActive?.id === tab.id ? 'border-white border-b-2 text-white' : 'border-b-2 border-transparent hover:border-blue-300/50 hover:border-b-2'"
                >
                {{ tab.title }}
              </button>
            </div>
            <div>
              <h1 class="text-mobile-preset-2 md:text-tablet-preset-2 lg:text-desctop-preset-1">{{ tabsActive?.title }}</h1>
              <p
                class="font-secondary font-normal border-b pb-10 border-white/50 text-blue-300 text-mobile-preset-9 md:text-tablet-preset-9 lg:text-desctop-preset-9 leading-[180%]">
                {{ tabsActive?.content }}
              </p>
              <div class="flex flex-col md:flex-row md:justify-around lg:justify-start lg:gap-10 uppercase">
                <div class="my-6 lg:my-10">
                  <div class="text-desctop-preset-8 font-tertiary text-blue-300/50 mb-3 tracking-[2px]">AVG. DISTANCE</div>
                  <div class="text-desctop-preset-6">{{ tabsActive?.distance }}</div>
                </div>
                <div class="my-6 lg:my-10">
                  <div class="text-desctop-preset-8 font-tertiary text-blue-300/50 mb-3 tracking-[2px]">Est. travel time</div>
                  <div class="text-desctop-preset-6">{{ tabsActive?.travelTime }}</div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

  </main>
</template>
