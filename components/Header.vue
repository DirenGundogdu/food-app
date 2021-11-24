<template>
  <v-container class="mt-2">
    <v-row no-gutters>
      <v-col cols="12" sm="6" md="8" class="d-flex justify-center align-center justify-md-start mb-4">
        <v-img
          max-height="150"
          max-width="150"
          :src="require('../static/logo.png')"
        ></v-img>
      </v-col>
      <v-col cols="12" md="4" class="d-flex justify-center align-center justify-md-end ">
        <v-btn class="mr-4 rounded-pill btn-blue" x-large>Login</v-btn>
        <v-btn class="rounded-pill btn-green" x-large>Sign In</v-btn>
      </v-col>
    </v-row>
    <!-- <v-app-bar elevation="0">
      <v-img
        max-height="150"
        max-width="150"
        :src="require('../static/logo.png')"
      ></v-img>
      <v-spacer></v-spacer>
      <v-btn class="mr-4 rounded-pill btn-blue" x-large>Login</v-btn>
      <v-btn class="rounded-pill btn-green" x-large>Sign In</v-btn>
    </v-app-bar> -->

   
  </v-container>
</template>

<script>
export default {}
</script>

<style scoped>
.v-app-bar,
.v-btn {
  background-color: transparent !important;
}
.btn-blue {
  border: 2px solid #0074d8;
  /* margin-right: 10px !important; */
}
.btn-green {
  border: 2px solid #01ff70;
}
</style>
