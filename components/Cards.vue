<template>
  <v-container>
    <v-row no-gutters>
      <v-col v-for="(imges,idx) in images" :key="idx" cols="12" sm="4">      
        <v-card :loading="loading" class="mx-auto my-4" max-width="374">
          <template slot="progress">
            <v-progress-linear
              color="deep-purple"
              height="10"
              indeterminate
            ></v-progress-linear>
          </template>
          <v-img height="250" :src="imges.foodImg"></v-img>          
          <v-card-title> {{ imges.foodName }}</v-card-title>

          <v-card-text>
            <v-row align="center" class="mx-0">
              <v-rating
                :value="1.5"
                color="#01ff70"
                dense
                half-increments
                readonly
                size="14"
              ></v-rating>

              <div class="grey--text ms-4">4.5 (413)</div>
            </v-row>

            <div class="my-4 text-subtitle-1">
              <span class="amber--text"> $ </span> •
              <span class="clr"> {{ imges.price }} </span>
            </div>

            <div class="heig">
              {{ imges.description}}
            </div>
          </v-card-text>

          <v-card-actions class="d-flex justify-end">
            <v-btn class="btn-grad" large rounded> Add to Card </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({
     images: [
       { foodImg: require('../static/food1.jpg'), foodName: 'Hamburger',price: 12,description: 'Classic Burger beef patty, crispy onions, sautéed mushrooms, cheddar cheese. With french fries'  },
       { foodImg: require('../static/food2.jpg'), foodName: 'Pizza',price: 18,description:'Special pizza sauce, mozzarella cheese, pepperoni, sausage, onion, sausage' },
       { foodImg: require('../static/food3.jpg'), foodName: 'Meat',price: 30,description: 'Chef meatballs, Beef Turkish Delight, Creamed Spinach, Baked Potato, Hot Sauce' },
       { foodImg: require('../static/food4.jpg'), foodName: 'Salmon',price: 15,description: 'fresh salmon and salad' },
       { foodImg: require('../static/food5.jpg'), foodName: 'Pancakes',price: 6,description: '2 pancakes, strawberry, banana, maple syrup (maple syrup), coconut powder upon request' },
       { foodImg: require('../static/food6.jpg'), foodName: 'Pasta',price: 8,description: 'Chicken, white pesto sauce, parmesan cheese' },
       { foodImg: require('../static/food7.jpg'), foodName: 'Tiramisu',price: 7,description: ''},
       { foodImg: require('../static/food8.jpg'), foodName: 'Sushi',price: 43,description:'Crab sticks, cucumber, avocado, tobiko' },
     ],
  }),
}
</script>

<style>
.btn-grad {
  background-image: linear-gradient(
    to right,
    #1d976c 0%,
    #93f9b9 51%,
    #1d976c 100%
  );
}
.btn-grad {
  margin: 10px;
  padding: 15px 45px;
  text-align: center;
  text-transform: uppercase;
  transition: 0.5s;
  background-size: 200% auto;
  color: white;
  box-shadow: 0 0 20px #eee;
  border-radius: 10px;
  display: block;
}

.btn-grad:hover {
  background-position: right center; /* change the direction of the change here */
  color: #fff;
  text-decoration: none;
}
.clr {
  color: #0074d8;
}
.heig {
  min-height: 44px !important;
}
</style>
