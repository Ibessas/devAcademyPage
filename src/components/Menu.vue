<template>
  <div>
    <div class="menu">
        <div class="nav" v-bind:style="navBackground">
            <div class="list">
                <ul>
                    <li>
                        <a href="#">Contato</a>
                    </li>
                    <li>
                        <a href="#">Localização</a>
                    </li>
                    <li>
                        <a href="#">Quem somos</a>
                    </li>
                    <li>
                        <a href="#">DevAcademy</a>
                    </li>
                </ul>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
    name: 'Menu',
    data() {
        return {
            navBackground:{
                backgroundColor:'rgba(255, 0, 0, 0)'
            }
        };
    },
    created () {
        window.addEventListener('scroll', this.handleScroll);
    },
    destroyed () {
        window.removeEventListener('scroll', this.handleScroll);
    },
    methods:{
        handleScroll () {
            this.navBackground.backgroundColor=`rgba(0, 0, 0,${window.scrollY/1000})`
        }
    }
};
</script>

<style lang="stylus">
.menu
    height 100%
    width 100%

.nav
    padding 1px 0px
    margin 0px
    position fixed
    top 0
    right 0

ul
    list-style-type none
    margin 0
    padding 1
    overflow hidden

li
    float right
    margin-right 10px
li a
    font-size 1.3vw
    display block
    color white 
    text-align center
    padding 14px 16px
    text-decoration none

li a:hover
    background-color white
    color black
    
</style>
