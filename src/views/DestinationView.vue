<script setup>
import { ref } from "vue";


const tabs = ref([
  { id: 1, title: 'MOON', content: 'content' },
  { id: 2, title: 'MARS', content: 'content' },
  { id: 3, title: 'EUROPA', content: 'content' },
  { id: 4, title: 'TITAN', content: 'content' },
]);

</script>

<template>
  <main
    class="h-max-screen bg-[url(@/assets/images/destination/background-destination-mobile.jpg)] md:bg-[url(@/assets/images/destination/background-destination-tablet.jpg)] lg:bg-[url(@/assets/images/destination/background-destination-desktop.jpg)] bg-no-repeat bg-cover bg-blue-900">
    <div class="flex items-center justify-center min-h-screen pt-40">
      <div class="container lg:max-w-lg text-center md:text-left text-white">
        <h2 class="my-6 text-mobile-preset-6 md:text-tablet-preset-5 lg:text-desctop-preset-5">
          <span class="mr-6 text-white/40 font-bold">01</span>PICK YOUR DESTINATION
        </h2>
        <div class="grid lg:grid-cols-2 md:px-16 lg:px-0 gap-8 justify-between">
          <div class="flex justify-start relative">
            <img class="z-10 mx-auto w-[228px] md:w-[458px] lg:w-auto " src="@/assets/images/destination/image-moon.png" alt="Moon">
          </div>
          <div class="text-center lg:text-left">
            <div class="flex justify-center lg:justify-start items-center gap-8">
              <button v-for="tab in tabs" :key="tab.id" class="cursor-pointer text-mobile-preset-8 md:text-desctop-preset-8" data-tab="tab1"> {{ tab.id }}
                {{ tab.title }}</button>
            </div>
            <div class="flex justify-center lg:justify-start items-center gap-8">
              <div v-for="tab in tabs" :key="tab.id">
                {{ tab.id }}
                {{ tab.content }}
              </div>
            </div>
            <h1 class="text-mobile-preset-2 md:text-tablet-preset-2 lg:text-desctop-preset-1">MOON</h1>
            <p class="border-b pb-10 border-white/50 text-blue-300 text-mobile-preset-9 md:text-tablet-preset-9 lg:text-desctop-preset-9">See our planet as you’ve never
              seen it before. A perfect relaxing trip away to help regain perspective
              and come back refreshed. While you’re there, take in some history by visiting the Luna 2 and Apollo 11
              landing sites.
            </p>
            <div class="flex flex-col md:flex-row md:justify-around lg:justify-start lg:gap-10 uppercase">
              <div class="my-6 lg:my-10">
                <div class="text-desctop-preset-7 font-primary text-blue-300/50 mb-3">AVG. DISTANCE</div>
                <div class="text-desctop-preset-6">384,400 km</div>
              </div>
              <div class="my-6 lg:my-10">
                <div class="text-desctop-preset-7 font-primary text-blue-300/50 mb-3">Est. travel time</div>
                <div class="text-desctop-preset-6">3 days</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

  </main>
</template>
