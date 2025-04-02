<script setup>
import { onMounted, ref } from "vue";

const tabsActive = ref(null);
const tabs = ref([
  {
    id: 1, supTitle:'Commander',
    title: 'Douglas Hurley',
    content: 'Douglas Gerald Hurley is an American engineer, former Marine Corps pilot and former NASA astronaut. He launched into space for the third time as commander of Crew Dragon Demo-2.',
    imgUrl: '/images/crew/image-douglas-hurley.png'
  },
  {
    id: 2, supTitle:'Mission Specialist',
    title: 'Mark Shuttleworth',
    content: 'Mark Richard Shuttleworth is the founder and CEO of Canonical, the company behind the Linux-based Ubuntu operating system. Shuttleworth became the first South African to travel to space as a space tourist.',
    imgUrl: '/images/crew/image-mark-shuttleworth.png'
  },
  {
    id: 3, supTitle:'Pilot',
    title: 'Victor Glover',
    content: 'Pilot on the first operational flight of the SpaceX Crew Dragon to the International Space Station. Glover is a commander in the U.S. Navy where he pilots an F/A-18.He was a crew member of Expedition 64, and served as a station systems flight engineer.',
    imgUrl: '/images/crew/image-victor-glover.png'
  },
  {
    id: 4, supTitle:'Flight Engineer',
    title: 'Anousheh Ansari',
    content: 'Anousheh Ansari is an Iranian American engineer and co-founder of Prodea Systems. Ansari was the fourth self-funded space tourist, the first self-funded woman to fly to the ISS, and the first Iranian in space.',
    imgUrl: '/images/crew/image-anousheh-ansari.png'
  },

]);

onMounted(() => {
  tabsActive.value = tabs.value[0]
})

</script>
<template>
  <main
    class="h-max-screen bg-[url(@/assets/images/crew/background-crew-mobile.jpg)] md:bg-[url(@/assets/images/crew/background-crew-tablet.jpg)] lg:bg-[url(@/assets/images/crew/background-crew-desktop.jpg)] bg-no-repeat bg-cover bg-blue-900">
    <div class="flex items-center justify-center min-h-screen pt-20 lg:pt-40">
      <div class="container lg:max-w-lg text-center lg:text-left text-white">
        <h2 class="my-6 md:text-left text-mobile-preset-6 md:text-tablet-preset-5 lg:text-desctop-preset-5 font-tertiary tracking-[4px]">
          <span class="mr-6 text-white/50 font-tertiary font-bold tracking-[4px]">02</span> MEET YOUR CREW
        </h2>
        <div class="grid lg:grid-cols-2 md:px-16 lg:px-0 gap-8 justify-between">
          <div class="my-8">
            <h2 class="text-mobile-preset-4 md:text-desctop-preset-4 uppercase text-white/50">{{tabsActive?.supTitle}}</h2>
            <h1 class="text-mobile-preset-3 md:text-desctop-preset-3 uppercase">{{ tabsActive?.title }}</h1>
            <p class="text-mobile-preset-9 md:text-tablet-preset-9 lg:text-desctop-preset-9 leading-[180%] text-blue-300 my-6 font-secondary font-normal">
              {{ tabsActive?.content }}
            </p>
            <div class="flex justify-center lg:justify-start items-center gap-4 md:gap-8 mt-10 md:20">
              <button v-for="tab in tabs" :key="tab.id" @click="tabsActive = tab"
                class="cursor-pointer text-blue-300 pb-2 text-mobile-preset-8 md:text-desctop-preset-8 w-[10px] h-[10px] md:w-[15px] md:h-[15px] rounded-full bg-blue-300/50"
                :class="tabsActive?.id === tab.id ? 'bg-white' : 'border-b-2 border-transparent hover:border-blue-300/50 hover:border-b-2'"
                >

              </button>
            </div>
          </div>
          <div class="flex justify-end relative">
            <img class="z-10 mx-auto w-[272px] md:w-[446px] lg:w-auto" :src="tabsActive?.imgUrl" alt="Moon">
          </div>
        </div>
      </div>
    </div>
  </main>
</template>
