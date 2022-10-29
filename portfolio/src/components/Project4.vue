<template>

  <v-container fill-height fluid>

    <!--top button-->
    <v-row :class="`animate__animated ${in_anim} d-flex align-top mt-4`" justify="center" v-if="this.$vuetify.breakpoint.name == 'xs'">
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
    <!-- <v-row :class="`animate__animated ${in_anim} d-flex align-top mt-4`" justify="center" v-else-if="this.$vuetify.breakpoint.name == 'xl'">
      <v-btn
        depressed
        fab
        icon
        outlined
        x-large
        class="text-bold"
        style="transform: scale(2);"
        @click="parentSwitchAnimation(1); updateValue(projectNum-1)"
      ><h6>Prev</h6></v-btn>
    </v-row> -->
    <v-row :class="`animate__animated ${in_anim} d-flex ml-4 align-top`" justify="center" v-else>
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

    <!--content-->
    <v-row :class="`animate__animated ${in_anim} d-flex ml-1 align-center`" justify="center" v-if="this.$vuetify.breakpoint.name == 'xs'">
        <v-col col="6" class="mt-10">
            <h1 class="text-h5">Vlad-Search</h1>
            <h3 class="text-subtitle-1 mt-4">A small Web Search Engine project. Can be used to search for any public domains on the world wide web.</h3>
            <h3 class="subtitle-1 mt-4">• Developed using bing's web search API</h3>
            <h3 class="subtitle-1">• Tools used: VueJS and Quasar</h3>
            <h3 class="subtitle-1">• Optimized for various screen sizes</h3>
            <div class="text-center">

              <a style="text-decoration: none;color: inherit;" href="https://github.com/vpik009/Vlad-Search" target="_blank">
                <v-btn depressed
                  class="mt-10 mr-1"
                >
                  View Source Code
                </v-btn>
              </a>

              <a style="text-decoration: none;color: inherit;" href="https://vpik009.github.io/Vlad-Search" target="_blank">
                <v-btn
                  class="mt-10 ml-1"
                  outlined
                  color="indigo"
                >
                  View Project
                </v-btn>
              </a>

            </div>
        </v-col>
        <v-col col="6" class="mt-10">
            <v-progress-circular
              v-if="loadingImage"
              indeterminate
              color="grey"
            ></v-progress-circular>
            <v-img
                v-else
                lazy-src="../assets/vlad-searchfinal_lazy.png"
                max-height="320"
                max-width="320"
                src="../assets/vlad-searchfinal.png"
                class="rounded-xl justify-center mb-10"
            ></v-img>
        </v-col>
    </v-row>
    <!-- <v-row :class="`animate__animated ${in_anim} d-flex ml-1 align-center`" justify="center" v-else-if="this.$vuetify.breakpoint.name == 'xl'">
        <v-col col="6">
            <h1 class="text-h3">Vlad-Search</h1>
            <h3 class="text-h4 mt-4">A small Web Search Engine project. Can be used to search for any public domains on the world wide web.</h3>
            <h3 class="text-h5 mt-4">• Developed using bing's web search API</h3>
            <h3 class="text-h5">• Tools used: VueJS and Quasar</h3>
            <h3 class="text-h5">• Optimized for various screen sizes</h3>
            <div class="text-center mt-10">

              <a style="text-decoration: none;color: inherit;" href="https://github.com/vpik009/Vlad-Search" target="_blank">
                <v-btn depressed
                  class="mt-4 ml-16"
                >
                  View Source Code
                </v-btn>
              </a>

              <a style="text-decoration: none;color: inherit;" href="https://vpik009.github.io/Vlad-Search" target="_blank">
                <v-btn
                  class="mt-4 ml-16"
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
                max-height="1000"
                max-width="1000"
                src="../assets/vlad-searchfinal.png"
                class="rounded-xl justify-center ml-16"
            ></v-img>
        </v-col>
    </v-row> -->
    <v-row :class="`animate__animated ${in_anim} d-flex ml-4 align-center`" justify="center" v-else>
        <v-col col="6">
            <h1 class="text-h3">Vlad-Search</h1>
            <h3 class="text-h5 mt-4">A small Web Search Engine project. Can be used to search for any public domains on the world wide web.</h3>
            <h3 class="subtitle-1 mt-4">• Developed using bing's web search API</h3>
            <h3 class="subtitle-1">• Tools used: VueJS and Quasar</h3>
            <h3 class="subtitle-1">• Optimized for various screen sizes</h3>
            <div class="text-center mt-10">

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
            <v-progress-circular
              v-if="loadingImage"
              indeterminate
              color="grey"
            ></v-progress-circular>
            <v-img
                v-else
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

    mounted: function () {
      this.$nextTick(function () {
        // Code that will run only after the
        // entire view has been rendered
        this.loadingImage = false;
      })
    },

    data: () => ({
      loadingImage: true,
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
