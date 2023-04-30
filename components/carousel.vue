<template>
  <v-carousel
    cycle
    height="250"
    hide-delimiter-background
    show-arrows="hover"
    max-width="800"
  >
    <v-carousel-item
      v-for="(slide, i) in slides"
      :key="i"
    >
        <v-img :src="slide.src" :contain="true" class="mx-auto" max-width="800" cover></v-img>
    </v-carousel-item>
  </v-carousel>
</template>
<script>
export default {
  data() {
    return {
      slides: [
         {
            src: '/slides/1.jpg',
          },
         {
            src: '/slides/2.jpg',
          },
          {
            src: '/slides/3.jpg',
          },
      
      ],
    }
  },
}
</script>