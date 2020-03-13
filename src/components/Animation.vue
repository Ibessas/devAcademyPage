<template>
  <div class="animation">
    <!-- <h1 class="group0">#</h1>
    <h1 class="group1">-</h1>
    <h1 class="group2">{</h1>
    <h1 class="group3">#</h1>
    <h1 class="group4">-</h1>
    <h1 class="group5">\</h1>
    <h1 class="group6">//</h1>
    <h1 class="group7">if</h1>
    <h1 class="group8">}</h1>
    <h1 class="group9">elif</h1> -->

  </div>
</template>

<script>
export default {
  name: 'Animation'
};
</script>

<style lang="stylus">
.animation
  height 100%
  width 100%
  color white
  bottom:15%;
  position absolute
  top 0
  z-index 0

h1
  position relative
  font-size 50px
  opacity 0.2

  -webkit-animation:linear infinite alternate;
  -webkit-animation-name: run;

.group1
  -webkit-animation-duration: 5s;

.group2
  -webkit-animation-duration: 20s;

.group3
  -webkit-animation-duration: 8s;

.group4
  -webkit-animation-duration: 16s;

.group5
  -webkit-animation-duration: 18s;

.group6
  -webkit-animation-duration: 9s;

.group7
  -webkit-animation-duration: 14s;

.group8
  -webkit-animation-duration: 15s;

.group9
  -webkit-animation-duration: 7s;

.group0
  -webkit-animation-duration: 6s;

@-webkit-keyframes run
    0% { left: 0;}
    50%{ left : 100%;}
    100%{ left: 0;}
</style>
