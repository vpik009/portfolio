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
            <h1 class="text-h3">AI Conversation Agent for Heart Disease Patients</h1>
            <h3 class="text-h5 mt-4">An AI conversational agent aimed at helping heart disease patients stay motivated to adhere to their medication.</h3>
            <h3 class="subtitle-1 mt-4">• Developed using AWS Lex and DynamoDB</h3>
            <h3 class="subtitle-1">• Initially used Firebase then migrated to DynamoDB</h3>
            <h3 class="caption mt-4">[Not open source as the project may potentially be used as a real product in the future]</h3>
        </v-col>
        <v-col col="6" class="ml-10">
            <v-img
                lazy-src="../assets/MARIAfinal_lazy.png"
                max-height="700"
                max-width="700"
                src="../assets/MARIAfinal.png"
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
    name: 'ProjectTwo',

    data: () => ({
      projectNum: 2
    }),
    props: ['val'],
    methods: {
      updateValue: function (value) {
        this.$emit('input', value);
      }
    }
  }
</script>
