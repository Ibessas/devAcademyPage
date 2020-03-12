<template>
  <div>
    <div class="capa" id="capa">
      <img v-bind:style='imgBackground' src='../assets/background1.png' alt="" srcset="">
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
      const valor = Math.abs((window.scrollY - 1000))/1000;
      this.imgBackground.opacity = valor
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
</style>
