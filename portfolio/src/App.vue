<template>
  <div id="app">

    <div class="md-layout md-gutter">
      <div class="md-layout-item md-size-55">
        <p class="md-display-4 animate__animated animate__backInLeft" style="font-family: URW Chancery L, cursive; color:#415380">Vladislav Pikulin</p>
        <p class="md-display-1 animate__animated animate__backInLeft" style="font-family: URW Chancery L, cursive; color:#415380">text about me...</p>
      </div>
      <div class="md-layout-item md-size-30">
        <img class="animate__animated  animate__backInUp" src="./components/back.jpg" style="width:625px;height:500px; border-radius: 200px;">
      </div>
    </div>

  </div>
</template>

<script>
import 'animate.css';

export default {
  name: 'App',
}
</script>

<style>
body{
  background-color: #f2f2f2;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
:root {
  --animate-duration: 1100ms;
  --animate-delay: 0.9s;
}
</style>
