<template>
  <div>
    <div class="capa">
      <img src='../assets/background1.png' alt="" srcset="">
      <Menu />
    </div>
  </div>
</template>

<script>
import Menu from './Menu.vue';

export default {
  name: 'Capa',
  components: {
    Menu
  }
};
</script>

<style lang="stylus">
.capa
  width 100%
  height auto
  position relative
  overflow hidden
  background-repeat no-repeat
img 
  width 100vw
</style>
