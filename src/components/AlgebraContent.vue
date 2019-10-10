<template>
  <v-container>
    <h1 class="display-4">Linear Equations in 2D</h1>
    <!-- <h4 class="display-1">Tags</h4> -->
    <div class="mt-4 mb-12 tags">
      <v-chip class="ma-2" color="primary" text-color="white" >
        Middle School Math
      </v-chip>
      <v-chip class="ma-2" color="deep-purple accent-4" outlined>
        Algebra
      </v-chip>
      <v-chip class="ma-2" color="indigo darken-3" outlined>
        Functions and Graphs
      </v-chip>
    </div>

    <v-card class="pa-4 mt-6 mb-12" max-width="pa-2" elevation="12">
      <v-card-title>What is a Linear Equation?</v-card-title>
      <v-card-text class="body-1 font-weight-regular">A linear equation is any equation that can be written in the format
         <span class="highlight-1">a<var>x</var> + b<var>y</var> = c (Standard Form)</span>, or its equivalent forms, such as 
         <span class="highlight-1"><var>y</var> = m<var>x</var> + b</span> (Slope-intercept Form). For the sake of simplicity,
         we will only be focusing on linear equations of two variables, <var>x</var> and <var>y</var>.
      </v-card-text>
      <v-card-text class="body-1">
        Linear equations are <span class="font-weight-bold">first-order</span>, which means that none items
        variables are raised to a higher power. This means that <span class="highlight-2">the slope a linear function is constant</span>,
        so we end up with straight lines when we graph our function.
      </v-card-text>
    </v-card>

    <div class="pb-12"></div>

    <h3 class="display-3 mt-12 mb-6">Some Visualizations of Linear Equations</h3>
    <v-row class="mt-6 mb-12">
        <v-col cols="12" md="8">
          <iframe width=100% height="400" src="https://www.youtube.com/embed/xg9hxYE1vBc?rel=0&mute=1" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </v-col>
        <v-col cols="12" md="4">
          <v-card elevation="6" class="pa-2" tile>
            <v-card-title>What's Going On Here?</v-card-title>
            <v-card-text class="body-1">Provided are some visualizations of linear equations.
              In the top left corner of the video, the equation is shown for each function.
            </v-card-text>
                <v-alert color="blue-white" icon="mdi-pencil" prominent>
                  Try graphing some of the equations yourself!
                </v-alert>
              <v-alert elevation="3" border="left" class="mt-4" type="info">
                Notice how both the slope and the y-intercept affect the function.
            </v-alert>
          </v-card>
        </v-col>
    </v-row>    

    <div class="pb-12"></div>

    <h4 class="display-1 mb-6">Finding the y-Intercept From Standard Form</h4>

    <v-stepper v-model="e1">
      <v-stepper-header>
        <v-stepper-step :complete="e1 > 1" step="1">Set x to zero</v-stepper-step>
        <v-divider></v-divider>
        <v-stepper-step :complete="e1 > 2" step="2">Isolate y</v-stepper-step>
        <v-divider></v-divider>
        <v-stepper-step step="3">Calculate</v-stepper-step>
      </v-stepper-header>

      <v-stepper-items>
        <v-stepper-content step="1">
          <v-card class="mb-12" color="light-green lighten-3" height="200px"></v-card>
          <v-btn color="primary" @click="e1 = 2">
            Continue
          </v-btn>
        </v-stepper-content>
        <v-stepper-content step="2">
          <v-card class="mb-12" color="deep-purple accent-1" height="200px">
          </v-card>
          <v-btn color="primary" @click="e1 = 3">
            Continue
          </v-btn>
          <v-btn text @click="e1 = 1">Back</v-btn>
        </v-stepper-content>
        <v-stepper-content step="3">
          <v-card class="mb-12" color="orange lighten-2" height="200px">
          </v-card>
          <v-btn color="primary" @click="e1 = 1">
            Continue
          </v-btn>
          <v-btn text @click="e1 = 2">Back</v-btn>
        </v-stepper-content>
      </v-stepper-items>
    </v-stepper>
  
    <h3 class="display-3 mt-6 mb-6">Test Your Understanding</h3>

  </v-container>

</template>

<script>
export default {
  data() {
    return {
      e1: 0,
    }
  },
  components: {}
};
</script>

<style scoped>
.highlight-1 {
  background-color: #fff2ac;
  background-image: linear-gradient(to right, #ffe359 0%, #fff2ac 100%);
  padding: 0.2em;
  border-radius: 4px;
}

.highlight-2 {
  background-color: #BBDEFB;
  background-image: linear-gradient(to right, #90CAF9 0%, #BBDEFB 100%);
  padding: 0.2em;
  border-radius: 4px;
}

</style>

