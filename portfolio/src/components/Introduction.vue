<template>
  <v-container fill-height fluid>
    <v-row class=" mt-16" justify="center">

        <div
          class=" animate__animated animate__backInUp text-h2"
          v-text="'Vladislav'"
        />

        <div
          class=" animate__animated animate__backInUp text-h2"
          v-text="''"
          style="width:1%;"
        />

        <div
          class="animate__animated animate__backInDown text-h2"
          v-text="'Pikulin'"
        />
        
    </v-row>
    <v-row class="animate__animated animate__fadeInUp animate__delay-1s" justify="center">
      <v-img
        lazy-src="../assets/vlad.jpg"
        max-height="400"
        max-width="500"
        src="../assets/vlad.jpg"
        class="rounded-xl justify-center"
      ></v-img>
    </v-row>
    <v-row class="animate__animated animate__fadeInUp animate__delay-1s" justify="center">
      <a style="text-decoration: none;color: inherit;" href="https://www.linkedin.com/in/vladislav-pikulin-77335821a/"><ion-icon size="large" name="logo-linkedin" class="mr-3"></ion-icon></a>
      <a style="text-decoration: none;color: inherit;" href="https://github.com/vpik009"><ion-icon size="large" name="logo-github" ></ion-icon></a>
      <a style="text-decoration: none;color: inherit;" href="https://drive.google.com/file/d/10VlmN5UvOiTZB8dY7IAikBf9b7kCYQN5/view?usp=sharing"><ion-icon size="large" name="attach-outline" class="ml-3"></ion-icon></a>
    </v-row>
    <v-row class="animate__animated animate__fadeInUp animate__delay-1s" justify="center">
      <v-btn
        depressed
        fab
        icon
        outlined
        x-large
        class="text-bold"
        @click="updateValue(projectNum+1)"
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
      }
    }
  }
</script>
