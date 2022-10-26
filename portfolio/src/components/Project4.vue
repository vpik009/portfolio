<template>

  <v-container fill-height fluid>

    <v-row :class="`animate__animated ${in_anim} d-flex ml-4 align-top`" justify="center">
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

    <v-row :class="`animate__animated ${in_anim} d-flex ml-4 align-center`" justify="center">
        <v-col col="6">
            <h1 class="text-h3">Vlad-Search</h1>
            <h3 class="text-h5 mt-4">A small Web Search Engine project. Can be used to search for any public domains on the world wide web.</h3>
            <h3 class="subtitle-1 mt-4">• Developed using bing's web search API</h3>
            <h3 class="subtitle-1">• Tools used: VueJS and Quasar</h3>
            <h3 class="subtitle-1">• Optimized for various screen sizes</h3>
            <div class="text-center">

              <a style="text-decoration: none;color: inherit;" href="https://github.com/vpik009/Vlad-Search" target="_blank">
                <v-btn depressed
                  class="mt-4 ml-4"
                >
                  View Source Code
                </v-btn>
              </a>

              <a style="text-decoration: none;color: inherit;" href="https://vpik009.github.io/Vlad-Search" target="_blank">
                <v-btn
                  class="mt-4 ml-4"
                  outlined
                  color="indigo"
                >
                  View Project
                </v-btn>
              </a>

            </div>
        </v-col>
        <v-col col="6" class="ml-10">
            <v-img
                lazy-src="../assets/vlad-searchfinal_lazy.png"
                max-height="700"
                max-width="700"
                src="../assets/vlad-searchfinal.png"
                class="rounded-xl justify-center"
            ></v-img>
        </v-col>
    </v-row>


    <v-row :class="`animate__animated ${in_anim} d-flex ml-4 align-bottom`" justify="center">
      <!-- <v-btn
        depressed
        fab
        icon
        outlined
        x-large
        class="text-bold"
        @click="parentSwitchAnimation(0); updateValue(projectNum+1)"
      ><h6>Next</h6></v-btn> -->
    </v-row>
    
  </v-container>
  
</template>

<script>
  export default {
    name: 'ProjectFour',

    data: () => ({
      projectNum: 4
    }),
    props: ['val','in_anim'],
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
