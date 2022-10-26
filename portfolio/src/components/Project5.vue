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
            <h1 class="text-h3">5. Title of the project</h1>
            <h3 class="text-h5 mt-4">Discussion here</h3>
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
    
  </v-container>
  
</template>

<script>
  export default {
    name: 'ProjectFive',

    data: () => ({
      projectNum: 5
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
