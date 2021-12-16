<template>
  <v-row justify="center" align="center">
    <v-col>
      <Header />
      <Carousel />

      <v-btn
        class="mt-5"
       depressed plain
  block
   text
  large
  rounded
>MENU</v-btn>

      <Cards />
    </v-col>
  </v-row>
</template>

<style scoped>
.v-btn {
  background-color: #536872;
  color: white;
  opacity: 1 !important;
}
.v-btn:hover {
   background-color:  #6e7f80;
}

</style>