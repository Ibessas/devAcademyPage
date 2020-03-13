<template>
      <div class="nav" v-bind:style="navBackground">
        <ul>
          <li><a href="#capa"> <span class="dev">dev.</span>academy</a></li>
          <li><a href="#">Quem somos</a></li>
          <li><a href="#time">Time</a></li>
          <li><a href="#">Sobre</a></li>
        </ul>
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

.nav
    width 100% 
    top 0px
    padding 10px 0px
    position fixed
    z-index 3

ul
  list-style-type none
  text-align center
  margin: 0 auto;
  padding: 0px;
  display:table;
  overflow: hidden;

li 
  margin-left: auto ;
  margin-right: auto ;
  float left

li a  
    font-weight: bold;  
    float left
    font-size 40px
    color white
    padding 5px 40px
    text-align center 
    text-decoration none
    border-radius   25px
  
.dev 
  color rgb(220, 178, 22)
.nav a:hover
    background-color rgba(255, 255, 255, 0.5 )


@media screen and (max-width: 600px) 
  .nav
    position relative
    top 0
  li a 
    font-size 20px
    border-radius 0px

</style>
