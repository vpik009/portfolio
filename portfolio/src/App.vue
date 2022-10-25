<template>
  <v-app>
    <v-main>
      {{ projectNum }}
      <transition
        mode="out-in"
        leave-active-class="animate__animated animate__fadeOutUp"
        v-if="projectNum==0">
        <Introduction v-model="projectNum" />
      </transition>
      <transition
        mode="out-in"
        enter-active-class="animate__animated animate__fadeIn"
        leave-active-class="animate__animated animate__fadeOutUp"
        v-else-if="projectNum==1">
        <Project1 v-model="projectNum"/>
      </transition>
      <transition
        mode="out-in"
        enter-active-class="animate__animated animate__fadeIn"
        leave-active-class="animate__animated animate__fadeOutUp"
        v-else-if="projectNum==2">
        <Project2 v-model="projectNum"/>
      </transition>
      <transition
        mode="out-in"
        enter-active-class="animate__animated animate__fadeIn"
        leave-active-class="animate__animated animate__fadeOutUp"
        v-else-if="projectNum==3">
        <Project3 v-model="projectNum"/>
      </transition>
      <transition
        mode="out-in"
        enter-active-class="animate__animated animate__fadeIn"
        leave-active-class="animate__animated animate__fadeOutUp"
        v-else-if="projectNum==4">
        <Project4 v-model="projectNum"/>
      </transition>
      <transition
        mode="out-in"
        enter-active-class="animate__animated animate__fadeIn"
        leave-active-class="animate__animated animate__fadeOutUp"
        v-else-if="projectNum==5">
        <Project5 v-model="projectNum"/>
      </transition>


    </v-main>
  </v-app>
</template>
<script>
import 'animate.css';
import Introduction from './components/Introduction.vue'
import Project1 from './components/Project1.vue'
import Project2 from './components/Project2.vue'
import Project3 from './components/Project3.vue'
import Project4 from './components/Project4.vue'
import Project5 from './components/Project5.vue'


export default {
  name: 'App',
  components:{
    Introduction,
    Project1,
    Project2,
    Project3,
    Project4,
    Project5
  },
  mounted() {
    let icons1 = document.createElement('script')
    icons1.setAttribute('src', "https://unpkg.com/ionicons@5.5.2/dist/ionicons/ionicons.js")
    document.head.appendChild(icons1)

    let icons2 = document.createElement('script')
    icons2.setAttribute('src', "https://unpkg.com/ionicons@5.5.2/dist/ionicons/ionicons.esm.js")
    document.head.appendChild(icons2)
  },

  data: () => ({
    screen_size: "lg", // xs,sm,md,lg,xl
    projectNum: 0  // 0 = intro, 1 = first project, 2 = second project ... etc
  }),
};
</script>
