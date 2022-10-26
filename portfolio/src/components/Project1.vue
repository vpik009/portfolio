<template>

  <v-container fill-height fluid>

    <v-row class="animate__animated animate__fadeInUp d-flex ml-4 align-top" justify="center">
      <v-btn
        depressed
        fab
        icon
        outlined
        x-large
        class="text-bold"
        @click="updateValue(projectNum-1)"
      ><h6>Intro</h6></v-btn>
    </v-row>

    <v-row class="animate__animated animate__fadeInUp d-flex ml-4 align-center justify-center" justify="center">
        <v-col col="6">
            <h1 class="text-h3">Full-Stack Developer - Intern</h1>
            <h3 class="text-h5 mt-4">Worked as an intern at CIBC Technology. Helped in the development of an e-commerce web application for building materials using VueJS, C# Entity-Framework,
and Signalr under the supervision of the senior project manager.</h3>
            <h3 class="caption mt-4">[Not open source as the work was done on a real application]</h3>

        </v-col>
        <v-col col="6" class="ml-10 justify-center">
            <v-img
                lazy-src="../assets/ebuildfinal.png"
                max-height="700"
                max-width="700"
                src="../assets/ebuildfinal.png"
                class="rounded-xl justify-center"
            ></v-img>
            
        </v-col>
    </v-row>

    <v-row class="animate__animated animate__fadeInUp d-flex ml-4 align-bottom" justify="center">
        <v-btn
            depressed
            fab
            icon
            outlined
            x-large
            class="text-bold"
            @click="updateValue(projectNum+1)"
        ><h6>Next</h6></v-btn>
    </v-row>
    
  </v-container>
  
</template>

<script>
  export default {
    name: 'ProjectOne',

    data: () => ({
      projectNum: 1
    }),
    props: ['val'],
    methods: {
      updateValue: function (value) {
        this.$emit('input', value);
      }
    }
  }
</script>
