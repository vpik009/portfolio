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
      ><h6>Prev</h6></v-btn>
    </v-row>

    <v-row class="animate__animated animate__fadeInUp d-flex ml-4 align-top" justify="center">
        <v-col col="6">
            <h1 class="text-h3">Web Application for Older Women</h1>
            <h3 class="text-h5 mt-4">A web application developed using HTML, CSS, JavaScript, JQuery, Google Firebase, and Google Firestore with a
Scrum-based Agile Framework. The application is aimed at providing a platform for older women to learn and experience
technology in a more suitable, for them, environment. This application was developed in a team of 16 members, divided into 3 subteams.
Our team was responsible for creating a Forum Module where users can discover posts made my others, and create their own.</h3>
        </v-col>
        <v-col col="6" class="ml-10">
            <v-img
                lazy-src="../assets/vlad.jpg"
                max-height="300"
                max-width="375"
                src="../assets/vlad.jpg"
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
    name: 'ProjectThree',

    data: () => ({
      projectNum: 3
    }),
    props: ['val'],
    methods: {
      updateValue: function (value) {
        this.$emit('input', value);
      }
    }
  }
</script>
