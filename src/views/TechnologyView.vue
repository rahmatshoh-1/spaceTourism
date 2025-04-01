<script setup>

</script>
<template>
  <main
    class="h-max-screen bg-[url(@/assets/images/technology/background-technology-mobile.jpg)] md:bg-[url(@/assets/images/technology/background-technology-tablet.jpg)] lg:bg-[url(@/assets/images/technology/background-technology-desktop.jpg)] bg-no-repeat bg-cover bg-blue-900">
    <div class="flex items-center justify-center min-h-screen lg:overflow-hidden pt-40">
      <div class="container lg:max-w-lg text-center lg:text-left text-white">
        <h2 class="my-6 md:text-left text-mobile-preset-6 md:text-tablet-preset-5 lg:text-desctop-preset-5"><span class="mr-6 text-white/40 font-bold">03</span>
          SPACE LAUNCH 101
        </h2>
        <div class="grid lg:grid-cols-2 lg:px-0 gap-8 justify-between">
          <div class="my-8 gap-8 flex flex-col lg:flex-row items-center order-2 lg:order-1">
            <div class="tab flex flex-row lg:flex-col items-center gap-8">
              <button class="w-10 h-10 md:w-14 md:h-14 lg:w-20 lg:h-20 rounded-full border text-mobile-preset-4 md:text-tablet-preset-4 lg:text-desctop-preset-4 bg-white text-black">1</button>
              <button class="w-10 h-10 md:w-14 md:h-14 lg:w-20 lg:h-20 rounded-full border text-mobile-preset-4 md:text-tablet-preset-4 lg:text-desctop-preset-4">2</button>
              <button class="w-10 h-10 md:w-14 md:h-14 lg:w-20 lg:h-20 rounded-full border text-mobile-preset-4 md:text-tablet-preset-4 lg:text-desctop-preset-4">3</button>
            </div>
            <div class="tabContent md:px-16 lg:px-0">
              <h2 class="text-mobile-preset-4 md:text-tablet-preset-4 lg:text-desctop-preset-4 uppercase text-white/50">THE TERMINOLOGY…</h2>
              <h1 class="text-mobile-preset-3 md:text-tablet-preset-3 lg:text-desctop-preset-3 uppercase whitespace-nowrap">LAUNCH VEHICLE</h1>
              <p class="text-mobile-preset-9 md:text-tablet-preset-9 lg:text-tablet-preset-9 text-blue-300 my-6 font-primary leading-7">
                A launch vehicle or carrier rocket is a rocket-propelled vehicle used to carry a payload from Earth's
                surface to space, usually to Earth orbit or beyond. Our WEB-X carrier rocket is the most powerful in
                operation. Standing 150 metres tall, it's quite an awe-inspiring sight on the launch pad!
              </p>
            </div>
          </div>
          <div class="flex justify-end relative order-1 lg:order-2">
            <img class="z-10 md:w-full lg:absolute lg:left-14 lg:-top-10" src="@/assets/images/technology/image-launch-vehicle-portrait.jpg" alt="Moon">
          </div>
        </div>
      </div>
    </div>
  </main>
</template>
