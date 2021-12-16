<template>
   <v-app >
      <v-main>
         <v-container fluid fill-height>
            <v-layout align-center justify-center>
               <v-flex xs12 sm8 md4>
                  <v-card class="elevation-12">
                     <v-toolbar color="#01ff70">
                        <v-toolbar-title class="title" >Sign In</v-toolbar-title>
                     </v-toolbar>
                     <v-card-text>
                     <form ref="form" @submit.prevent="login()">
                            <v-text-field
                              v-model="username"
                              name="username"
                              label="Username"
                              type="text"
                              placeholder="username"
                              required
                           ></v-text-field>
                           
                            <v-text-field
                              v-model="password"
                              name="password"
                              label="Password"
                              type="password"
                              placeholder="password"
                              required
                           ></v-text-field>

                              <v-text-field
                              v-model="repassword"
                              name="repassword"
                              label="Confirm Password"
                              type="password"
                              placeholder="confirm password"
                              required
                           ></v-text-field>
                           <div class="d-flex justify-end">
                               
                           <v-btn depressed plain class="mr-4 rounded-pill btn-blue" x-large>Login</v-btn>
                           </div>
                      </form>
                     </v-card-text>
                  </v-card>
                
               </v-flex>
            </v-layout>
         </v-container>
      </v-main>
   </v-app>
</template>

<script>
export default {
  name: "Login",
  data() {
    return {
      username: "",
      password: "",
      repassword: "",
    };
  },
//   methods: {
//     login() {
//       const { username } = this;
//       console.log(username + "logged in")
//     },
//   },
};
</script>

<style scoped>
.v-app-bar,
.v-btn {
  border: 2px solid #01ff70;

  color: black !important;
}
.btn-blue:hover {
  background-color: #01ff70;
  
  color: white !important;
}
.title {
    color: white !important;
}
</style>
