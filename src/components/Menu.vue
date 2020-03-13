<template>
      <div class="nav" v-bind:style="navBackground" v-bind:class="{'responsive':responsive}">
        <ul>
          <li><a href="#capa"> <span class="dev">dev.</span>academy</a></li>
          <li><a href="#">Quem somos</a></li>
          <li><a href="#time">Time</a></li>
          <li><a href="#">Sobre</a></li>
          
        </ul>
          <a class="icon" @click="toggleNav">&#9776;</a>
      </div> 
</template>

<script>
export default {
  name: 'Menu',
  data() {
    return {
      navBackground: {
        backgroundColor: 'rgba(255, 0, 0, 0)'
      },
      responsive:false
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
      if(window.screen.width < 1020)
        this.navBackground.backgroundColor = `rgba(0, 0, 0,${window.scrollY / 150})`;
      else
        this.navBackground.backgroundColor = `rgba(0, 0, 0,${window.scrollY / 1000})`;

    },
    toggleNav(){
      this.responsive = !this.responsive
      if(this.responsive)
        this.navBackground.backgroundColor = `rgba(0, 0, 0,1)`;
      else
        this.handleScroll()
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
    font-size 2vw
    color white
    padding 5px 40px
    text-align center 
    text-decoration none
    border-radius   25px
  
.dev 
  color rgb(220, 178, 22)

.nav a:hover
    background-color rgba(255, 255, 255, 0.5 )

.icon
  display none


@media screen and (max-width: 1020px) 
  .nav
    position relative
    top 0

  ul
    margin 0
  li

    left 0
    float none

  li a 
    font-size 4vw
    border-radius 0px
  
  li:not(:first-child) 
    display none
  
  a.icon
    font-size 4vw
    position absolute
    right 0
    top 0
    padding 14px 14px
    color white
    float right
    display block 
    cursor pointer 

@media screen and (max-width: 1020px) 
  .nav 
    position fixed

  .responsive .icon 
    position: absolute;
    right: 0;
    top: 0;
  
  .responsive li 
    display block
    float: none;
    text-align: left;

</style>
