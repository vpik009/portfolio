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
        @click="parentSwitchAnimation(1); updateValue(projectNum-1)"
      ><h6>Prev</h6></v-btn>
    </v-row>

    <v-row class="animate__animated animate__fadeInUp d-flex ml-4 align-center" justify="center">
        <v-col col="6">
            <h1 class="text-h3">Vlad-Search</h1>
            <h3 class="text-h5 mt-4">A small Web Search Engine project. Can be used to search for any public domains on the world wide web.</h3>
            <h3 class="subtitle-1 mt-4">• Developed using bing's web search API</h3>
            <h3 class="subtitle-1">• Tools used: VueJS and Quasar</h3>
            <h3 class="subtitle-1">• Optimized for various screen sizes</h3>
        </v-col>
        <v-col col="6" class="ml-10">
            <v-img
                lazy-src="../assets/vlad_lazy.jpg"
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
        @click="parentSwitchAnimation(0); updateValue(projectNum+1)"
      ><h6>Next</h6></v-btn>
    </v-row>
    
  </v-container>
  
</template>

<script>
  export default {
    name: 'ProjectFour',

    data: () => ({
      projectNum: 4
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
