<template>
  <v-carousel
    :show-arrows="false"
    cycle
    height="500"
    width=
    hide-delimiter-background
    hide-delimiters
    class="rounded-xl"
  >
    <v-carousel-item
      v-for="(item, i) in items"
      :key="i"
      :src="item.src"
      reverse-transition="fade-transition"
      transition="fade-transition"
    ></v-carousel-item>
  </v-carousel>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          src: require('../static/sli1.jpg'),
        },
        {
          src: require('../static/sli2.jpg'),
        },
        {
          src: require('../static/sli3.jpg'),
        },
        {
          src: require('../static/sli4.jpg'),
        },
      ],
    }
  },
}
</script>
