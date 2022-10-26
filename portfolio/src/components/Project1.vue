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
      ><h6>Intro</h6></v-btn>
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
      ><h6>Intro</h6></v-btn>
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
      ><h6>Intro</h6></v-btn>
    </v-row>


    <!--content-->
    <v-row :class="`animate__animated ${in_anim} d-flex ml-1 align-center`" justify="center" v-if="this.$vuetify.breakpoint.name == 'xs'">
        <v-col col="6" class="mt-6">
            <h1 class="text-h5">Full-Stack Developer - Intern</h1>
            <h3 class="text-subtitle-1 mt-4">Worked as an intern at CIBC Technology. Helped in the development of an e-commerce web application for building materials using VueJS, C# Entity-Framework,
and Signalr under the supervision of the senior project manager.</h3>
            <h3 class="caption mt-4">[Not open source as the work was done on a real application]</h3>

        </v-col>
        <v-col col="6" class="justify-center">
            <v-img
                lazy-src="../assets/ebuildfinal_lazy.png"
                max-height="320"
                max-width="320"
                src="../assets/ebuildfinal.png"
                class="rounded-xl justify-center"
            ></v-img>
            
        </v-col>
    </v-row>
    <!-- <v-row :class="`animate__animated ${in_anim} d-flex ml-1 align-center`" justify="center" v-else-if="this.$vuetify.breakpoint.name == 'xl'">
        <v-col col="6" class="mt-6 ml-6">
            <h1 class="text-h3">Full-Stack Developer - Intern</h1>
            <h3 class="text-h4 mt-4">Worked as an intern at CIBC Technology. Helped in the development of an e-commerce web application for building materials using VueJS, C# Entity-Framework,
and Signalr under the supervision of the senior project manager.</h3>
            <h3 class="text-subtitle-1 mt-4">[Not open source as the work was done on a real application]</h3>

        </v-col>
        <v-col col="6" class="justify-center">
          <div>
            <v-img
                lazy-src="../assets/ebuildfinal_lazy.png"
                max-height="1000"
                max-width="1000"
                src="../assets/ebuildfinal.png"
                class="rounded-xl justify-center ml-16"
            ></v-img>
          </div>
            
        </v-col>
    </v-row> -->
    <v-row :class="`animate__animated ${in_anim} d-flex ml-4 align-center`" justify="center" v-else>
        <v-col col="6">
            <h1 class="text-h3">Full-Stack Developer - Intern</h1>
            <h3 class="text-h5 mt-4">Worked as an intern at CIBC Technology. Helped in the development of an e-commerce web application for building materials using VueJS, C# Entity-Framework,
and Signalr under the supervision of the senior project manager.</h3>
            <h3 class="caption mt-4">[Not open source as the work was done on a real application]</h3>

        </v-col>
        <v-col col="6" class="ml-10 justify-center">
            <v-img
                lazy-src="../assets/ebuildfinal_lazy.png"
                max-height="700"
                max-width="700"
                src="../assets/ebuildfinal.png"
                class="rounded-xl justify-center"
            ></v-img>
            
        </v-col>
    </v-row>


    <!--bottom button-->
    <v-row :class="`animate__animated ${in_anim} d-flex ml-1 align-bottom mt-16 mb-4`" justify="center" v-if="this.$vuetify.breakpoint.name == 'xs'">
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
    <!-- <v-row :class="`animate__animated ${in_anim} d-flex ml-1 align-bottom mt-4 mb-4`" justify="center" v-else-if="this.$vuetify.breakpoint.name == 'xl'">
        <v-btn
            depressed
            fab
            icon
            outlined
            x-large
            class="text-bold"
            style="transform: scale(2);"
            @click="parentSwitchAnimation(0); updateValue(projectNum+1)"
        ><h6>Next</h6></v-btn>
    </v-row> -->
    <v-row :class="`animate__animated ${in_anim} d-flex ml-4 align-bottom`" justify="center" v-else>
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
    name: 'ProjectOne',

    data: () => ({
      projectNum: 1,
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
