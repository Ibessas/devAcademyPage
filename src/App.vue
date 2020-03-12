<template>
  <div id="app">
    <Capa />
    <Team/>
    <Animation />


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
body
  margin: 0
  font-family dekar-regular
  height 5000px
  background-color black

@font-face
  font-family: dekar-regular;
  src: url('./assets/Dekar/Dekar-Regular.otf');
</style>
