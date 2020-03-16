<template>
  <div class="capa" id="capa">
    <Menu />
    <img
      class="background"
      v-bind:style="imgBackground"
      src="../assets/background1.png"
      alt=""
      srcset=""
    />
  </div>
</template>

<script>
import Menu from './Menu.vue';

export default {
  name: 'Capa',
  components: {
    Menu
  },
  data() {
    return {
      imgBackground: {
        opacity: '1'
      }
    };
  },
  created() {
    window.addEventListener('scroll', this.handleScroll);
  },
  destroyed() {
    window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll() {
      let valor = Math.abs(window.scrollY - 1000) / 1000;
      if (valor < 0.4) valor /= 2;
      this.imgBackground.opacity = valor;
    }
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
  z-index -1
  position relative
Menu
  z-index 0

@media screen and (max-width: 600px)
  .background
    width 200vw
    margin-left -50vw
</style>
