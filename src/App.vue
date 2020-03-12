<template>
  <div id="app">
    <Capa />
  </div>
</template>

<script>
import Capa from './components/Capa.vue';

export default {
  name: 'App',
  components: {
    Capa
  }
};
</script>

<style lang="stylus">
body
  margin: 0
  font-family dekar-regular
  height 5000px

@font-face
  font-family: dekar-regular;
  src: url('./assets/Dekar/Dekar-Regular.otf');
</style>
