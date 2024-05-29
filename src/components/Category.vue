<script setup>
  import category1 from "../assets/images/category/fg.jpg"
  import category2 from "../assets/images/category/v.jpg"
  import category3 from "../assets/images/category/login-bg.png"

  const categories = [
    {
      title: 'Colors',
      image: category1,
      desc: 'Colors are fascinating and integral to our perception of the world around us. They are visual sensations that arise from the way our eyes perceive different wavelengths of light. In the visible spectrum, there are numerous colors, each possessing unique properties and evoking distinct emotions and associations.'
    },
    {
      title: '3D Images',
      image: category2,
      desc: 'Three-dimensional (3D) images are visual representations that simulate depth perception, giving the illusion of objects existing in three dimensions. Unlike two-dimensional (2D) images, which only have length and width, 3D images add the element of depth, creating a more immersive and realistic experience.'
    },
    {
      title: 'Animation',
      image: category3,
      desc: 'Three-dimensional (3D) animation is a process of creating moving images in a three-dimensional digital environment. It involves the use of computer graphics to generate lifelike and dynamic visuals, allowing for the creation of realistic characters, objects, and environments.'
    },
  ]
</script>

<template>
  <section id="category" class="flex flex-col items-center py-32">
    <h2 class="my-10 text-5xl md:text-6xl font-bold text-white">Category</h2>
    <div class="grid grid-cols-1 md:grid-cols-3 place-items-center">
      <div v-for="category of categories" :key="category.title" class="text-white grid place-items-center gap-5 text-center">
        <div class="p-10">
          <img :src="category.image" class="w-full" alt="category1" style="width: 450px; height: 300px; border-radius: 20px;">
        </div>
        <h3 class="text-3xl font-bold">{{ category.title }}</h3>
        <p class="w-3/4" style="    text-align: justify;">{{ category.desc}}</p>
      </div>
    </div>
  </section>
  <section class="grid grid-flow-col grid-cols-1 md:grid-cols-2 md:gap-10 items-center">
    <div class="md:p-10">
      <img src="../assets/images/R.png" alt="category2-img">
    </div>
    <div class="text-center flex flex-col items-center">
      <h2 class="text-5xl md:text-6xl font-bold text-white">What's that</h2>
      <div class="flex items-center gap-5">
        <h2 class="text-5xl md:text-6xl font-bold text-white">3D BACKGROUND</h2>
        <img  class="w-9 md:w-12" alt="">
      </div>
      <p class="mt-8 md:mt-12 text-white text-lg md:text-xl w-full md:w-[80%]" style="text-align: justify;">3D backgrounds are commonly used in design and animation to create realistic and immersive environments. They are digital representations of three-dimensional spaces that can be used as backdrops or settings for various media such as video games, movies, architectural visualizations, and virtual reality experiences.</p>
    </div>
  </section>
</template>