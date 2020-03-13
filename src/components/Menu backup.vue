<template>
  <div>
    <div class="menu">
      <div class="nav" v-bind:style="navBackground">
              <a href="#">DevAcademy</a>
              <a href="#">Quem somos</a>
              <a href="#">Time</a>
              <a href="#">Sobre</a>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Menu',
  data() {
    return {
      navBackground: {
        backgroundColor: 'rgba(255, 0, 0, 0)'
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
      this.navBackground.backgroundColor = `rgba(0, 0, 0,${window.scrollY / 1000})`;
    }
  }
};
</script>

<style lang="stylus">
.menu
    height 100%
    width 100%

.nav
    width 100% 
    position fixed
    top 0
    overflow auto

.nav a  
    width 25%
    float left
    font-size 30px
    color white
    padding 15px 0px
    text-align center 
    text-decoration none

.nav a:hover
    background-color rgba(255, 255, 255, 0.5 )
</style>
