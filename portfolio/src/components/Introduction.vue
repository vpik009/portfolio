<template>
  <v-container fill-height fluid>
    
    <!--Name-->
      <!--XS-->
      <v-row class=" mt-10" justify="center" v-if="this.$vuetify.breakpoint.name == 'xs'">

        <div
          class=" animate__animated animate__backInUp text-h4"
          v-text="'Vladislav'"
        />

        <div
          class=" animate__animated animate__backInUp text-h2"
          v-text="''"
          style="width:3%;"
        />

        <div
          class="animate__animated animate__backInDown text-h4"
          v-text="'Pikulin'"
        />
        
    </v-row>
      <!--SM-->
      <!--MD-->
      <!--LG-->
    <v-row class=" mt-16" justify="center" v-else>

        <div
          class=" animate__animated animate__backInUp text-h2"
          v-text="'Vladislav'"
        />

        <div
          class=" animate__animated animate__backInUp text-h2"
          v-text="''"
          style="width:2%;"
        />

        <div
          class="animate__animated animate__backInDown text-h2"
          v-text="'Pikulin'"
        />
        
    </v-row>
    <!--XL-->
    <!-- <v-row class=" mt-16" justify="center" v-if="this.$vuetify.breakpoint.name == 'xl'">

        <div
          class=" animate__animated animate__backInUp text-h1"
          v-text="'Vladislav'"
        />

        <div
          class=" animate__animated animate__backInUp text-h1"
          v-text="''"
          style="width:1%;"
        />

        <div
          class="animate__animated animate__backInDown text-h1"
          v-text="'Pikulin'"
        />
        
    </v-row> -->

    <!-- <v-row class="animate__animated animate__fadeInUp animate__delay-1s" justify="center" v-if="this.$vuetify.breakpoint.name == 'xl'">
      <v-img
        lazy-src="../assets/vlad_lazy.jpg"
        max-height="800"
        max-width="1000"
        src="../assets/vlad.jpg"
        class="rounded-xl justify-center"
      ></v-img>
    </v-row> -->
    <v-row class="animate__animated animate__fadeInUp animate__delay-1s" justify="center">
      <v-img
        lazy-src="../assets/vlad_lazy.jpg"
        max-height="400"
        max-width="500"
        src="../assets/vlad.jpg"
        class="rounded-xl justify-center"
      ></v-img>
    </v-row>


    <!-- <v-row class="animate__animated animate__fadeInUp animate__delay-1s" justify="center" v-if="this.$vuetify.breakpoint.name == 'xl'">
      <a style="text-decoration: none;color: inherit;" href="https://www.linkedin.com/in/vladislav-pikulin-77335821a/" target="_blank"><ion-icon size="large" name="logo-linkedin" class="mr-16" style="transform: scale(2);"></ion-icon></a>
      <a style="text-decoration: none;color: inherit;" href="https://github.com/vpik009" target="_blank"><ion-icon size="large" name="logo-github" style="transform: scale(2);"></ion-icon></a>
      <a style="text-decoration: none;color: inherit;" href="https://drive.google.com/file/d/10VlmN5UvOiTZB8dY7IAikBf9b7kCYQN5/view?usp=sharing" target="_blank"><ion-icon size="large" name="attach-outline" class="ml-16" style="transform: scale(2);"></ion-icon></a>
    </v-row> -->
    <v-row class="animate__animated animate__fadeInUp animate__delay-1s" justify="center">
      <a style="text-decoration: none;color: inherit;" href="https://www.linkedin.com/in/vladislav-pikulin-77335821a/" target="_blank"><ion-icon size="large" name="logo-linkedin" class="mr-3"></ion-icon></a>
      <a style="text-decoration: none;color: inherit;" href="https://github.com/vpik009" target="_blank"><ion-icon size="large" name="logo-github" ></ion-icon></a>
      <a style="text-decoration: none;color: inherit;" href="https://drive.google.com/file/d/10VlmN5UvOiTZB8dY7IAikBf9b7kCYQN5/view?usp=sharing" target="_blank"><ion-icon size="large" name="attach-outline" class="ml-3"></ion-icon></a>
    </v-row>

    <!-- <v-row class="animate__animated animate__fadeInUp animate__delay-1s" justify="center" v-if="this.$vuetify.breakpoint.name == 'xl'">
      <v-btn
        depressed
        fab
        icon
        outlined
        x-large
        class="text-bold"
        style="transform: scale(2);"
        @click="parentSwitchAnimation(0), updateValue(projectNum+1)"
      ><h6>Projects</h6></v-btn>
    </v-row> -->
    <v-row class="animate__animated animate__fadeInUp animate__delay-1s" justify="center">
      <v-btn
        depressed
        fab
        icon
        outlined
        x-large
        class="text-bold"
        @click="parentSwitchAnimation(0), updateValue(projectNum+1)"
      ><h6>Projects</h6></v-btn>
    </v-row>
    
  </v-container>
  
</template>

<script>
  export default {
    name: 'IntroDuction',

    data: () => ({
      projectNum: 0
    }),
    props: ['val'],
    methods: {
      updateValue: function (value) {
        this.$emit('input', value);
      },
      parentSwitchAnimation(val){
        this.$emit('switchAnim',val);
      }
    }
  }
</script>
