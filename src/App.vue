<template>
  <div id="app">
    <Animation />
    <Capa />
    <span id="time"></span>
    <QuemSomos />
    <Team />
    <Rodape />
    <span id="rodape"></span>
  </div>
</template>

<script>
import Capa from './components/Capa.vue';
import Animation from './components/Animation.vue';
import Team from './components/team/Team.vue';
import Rodape from './components/Rodape.vue';
import QuemSomos from './components/quem-somos/QuemSomos.vue';

export default {
  name: 'App',
  components: {
    Capa,
    Animation,
    Team,
    Rodape,
    QuemSomos
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

.animation, .nav
  position fixed

#time
  display block
  height: 10px;
  visibility: hidden;

#rodape
  position absolute
  display block
  bottom 0
  visibility: hidden;
</style>
