<script setup>

</script>
<template>
  <main
    class="h-max-screen bg-[url(@/assets/images/crew/background-crew-mobile.jpg)] md:bg-[url(@/assets/images/crew/background-crew-tablet.jpg)] lg:bg-[url(@/assets/images/crew/background-crew-desktop.jpg)] bg-no-repeat bg-cover bg-blue-900">
    <div class="flex items-center justify-center min-h-screen pt-40">
      <div class="container lg:max-w-lg text-center lg:text-left text-white">
        <h2 class="my-6 md:text-left text-mobile-preset-6 md:text-tablet-preset-5 lg:text-desctop-preset-5">
          <span class="mr-6 text-white/40 font-bold">02</span> MEET YOUR CREW
        </h2>
        <div class="grid lg:grid-cols-2 md:px-16 lg:px-0 gap-8 justify-between">
          <div class="my-8">
            <h2 class="text-mobile-preset-4 md:text-desctop-preset-4 uppercase text-white/50">Commander</h2>
            <h1 class="text-mobile-preset-3 md:text-desctop-preset-3 uppercase">Douglas Hurley</h1>
            <p class="text-mobile-preset-9 md:text-tablet-preset-9 text-blue-300 my-6">
              Douglas Gerald Hurley is an American engineer, former Marine Corps pilot and former NASA astronaut. He
              launched into space for the third time as commander of Crew Dragon Demo-2.
            </p>

          </div>
          <div class="flex justify-end relative">
            <img class="z-10 mx-auto w-[272px] md:w-[446px] lg:w-auto" src="@/assets/images/crew/image-douglas-hurley.png" alt="Moon">
          </div>
        </div>
      </div>
    </div>
  </main>
</template>
