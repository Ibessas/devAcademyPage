<template>
  <div id="app">
    <Animation />
    <Capa/>
    <span id="time"></span>
    <Team/>


  </div>
</template>

<script>
import Capa from './components/Capa.vue';
import Animation from './components/Animation.vue';
import Team from './components/team/Team.vue'


export default {
  name: 'App',
  components: {
    Capa,
    Animation,
    Team

  }
};
</script>

<style lang="stylus">
html
  overflow-x hidden

body
  margin: 0
  font-family dekar-regular
  background-color black
  overflow-x hidden
  position relative
  z-index 0

@font-face
  font-family: dekar-regular;
  src: url('./assets/Dekar/Dekar-Regular.otf');

#time
  display block
  height: 10px;  
  visibility: hidden;
</style>
