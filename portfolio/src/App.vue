<template>
  <v-app>
    <v-main>
      
      <v-container fill-height fluid>
        <v-row class="d-flex justify-center align-center">

            <div
              class="animate__animated animate__backInUp d-flex text-h2 transition-swing mr-2"
              v-text="'Vladislav'"
            >
            </div>

            <div
              class="animate__animated animate__backInDown d-flex text-h2 transition-swing ml-2"
              v-text="'Pikulin'"
            >
            </div>
        </v-row>
      </v-container>

    </v-main>
  </v-app>
</template>

<script>
import 'animate.css';

export default {
  name: 'App',

  data: () => ({
    screen_size: "lg", // xs,sm,md,lg,xl
  }),
};
</script>
