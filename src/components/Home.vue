<script setup>
  import MySwiper from "./MySwiper.vue"
</script>

<template>
  <section id="home" class="grid place-items-center mt-20 md:mt-10 overflow-hidden">
    <div class="grid grid-flow-row-dense grid-cols-1 lg:grid-cols-2 items-end gap-10 lg:gap-16 w-full px-0 lg:px-10">
      <div class="text-5xl md:text-6xl font-bold text-white w-full pb-20 order-2 lg:order-1">
        <div class="flex items-center gap-3">
          <h2>3d background</h2>
        </div>
        <!-- <h2 class="text-4xl md:text-5xl">Or Three dimensional  </h2> -->
        <p class="pt-5 text-lg font-normal">In Computer Graphics and Animation , 3d background are created using specializtion softwire that allows artists to model and render three dimensional objects . and show the images for 3D   </p>
      </div>
      <div class="w-full h-full order-1 lg:order-2">
        <br>
        <br> <br> <br> <br><br><br><br>
        <MySwiper/>
      </div>
    </div>
  </section>

</template>