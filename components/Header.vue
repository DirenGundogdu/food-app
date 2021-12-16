<template>
  <v-container class="mt-2">
    <v-row no-gutters>
      <v-col cols="12" sm="6" md="8" class="d-flex justify-center align-center justify-md-start mb-4">
        <img
          max-height="150"
          max-width="150"
          src="../static/logo.png"
        />        
      </v-col>
      <v-col cols="12" md="4" class="d-flex justify-center align-center justify-md-end ">
        <v-btn depressed plain class="mr-4 rounded-pill btn-blue" x-large><nuxt-link to="/users/login" style="text-decoration: none; color: inherit;">Login</nuxt-link></v-btn>
        <v-btn depressed plain class="rounded-pill btn-green" x-large><nuxt-link to="/users/signin" style="text-decoration: none; color: inherit;">Sign In</nuxt-link></v-btn>
        
      </v-col>
    </v-row>   
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
.btn-blue:hover {
  border: 2px solid #0074d8;
}
.btn-green:hover {
  border: 2px solid #01ff70;
}
</style>