<template>
  <div>
    <div class="capa">
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
  height 100vw
  position relative
  overflow hidden
  background-image url('../assets/background.png')
  background-repeat no-repeat
</style>
