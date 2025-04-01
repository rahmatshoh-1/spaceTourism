<script setup>

</script>

<template>
  <main
    class="h-screen bg-[url(@/assets/images/home/background-home-mobile.jpg)] md:bg-[url(@/assets/images/home/background-home-tablet.jpg)] lg:bg-[url(@/assets/images/home/background-home-desktop.jpg)] bg-no-repeat bg-cover bg-blue-900">
    <div class="flex items-center justify-center min-h-screen lg:pt-40">
      <div class="container lg:max-w-lg text-white">
        <div class="grid lg:grid-cols-2 md:px-16 lg:px-0 gap-8 justify-between">
          <div class="text-center lg:text-left">
            <h2 class="text-mobile-preset-6 my-6 md:text-desctop-preset-5">SO, YOU WANT TO TRAVEL TO</h2>
            <h1 class="text-mobile-preset-1 mb-6 md:text-desctop-preset-1">SPACE</h1>
            <p class="text-mobile-preset-9 md:text-tablet-preset-9">
              Let’s face it; if you want to go to space, you might as well genuinely go to outer space and not hover
              kind of on the edge of it. Well sit back, and relax because we’ll give you a truly out of this world
              experience!
            </p>
          </div>
          <div class="flex justify-center lg:justify-end">
            <div
              class="group rounded-full h-[244px] w-[244px] md:h-[344px] md:w-[344px] hover:bg-white/20 transition-all duration-700 flex items-center justify-center">
              <RouterLink to="/destination"
                class="flex  items-center justify-center rounded-full h-[144px] w-[144px] md:h-[244px] md:w-[244px]  bg-white text-black font-bellefair text-mobile-preset-4 md:text-desctop-preset-4 tracking-[2px] transition-transform duration-300 cursor-pointer">
                EXPLORE
              </RouterLink>
            </div>
          </div>
        </div>
      </div>
    </div>

  </main>
</template>
