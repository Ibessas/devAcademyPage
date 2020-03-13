<template>
  <div>
    <div class="animation">

      <h1 class="group1">-</h1>
      <h1 class="group2">{</h1>
      <h1 class="group3">#</h1>
      <h1 class="group4">\</h1>
      <h1 class="group5">//</h1>
      <h1 class="group2">}</h1>
      <h1 class="group3">if</h1>
      <h1 class="group1">elif</h1>
      <h1 class="group5">-</h1>
      <h1 class="group4">#</h1>

      <h1 class="group1">-</h1>
      <h1 class="group2">{</h1>
      <h1 class="group3">#</h1>
      <h1 class="group4">\</h1>
      <h1 class="group5">//</h1>
      <h1 class="group2">}</h1>
      <h1 class="group3">if</h1>
      <h1 class="group1">elif</h1>
      <h1 class="group5">-</h1>
      <h1 class="group4">#</h1>

      <h1 class="group1">-</h1>
      <h1 class="group2">{</h1>
      <h1 class="group3">#</h1>
      <h1 class="group4">\</h1>
      <h1 class="group5">//</h1>
      <h1 class="group2">}</h1>
      <h1 class="group3">if</h1>
      <h1 class="group1">elif</h1>
      <h1 class="group5">-</h1>
      <h1 class="group4">#</h1>


    
    </div>
  </div>
</template>

<script>
export default {
  name: 'Animation',
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
  -webkit-animation-duration: 8s;
     
.group3
  -webkit-animation-duration: 15s;

.group4
  -webkit-animation-duration: 12s;

.group5
  -webkit-animation-duration: 18s;
     
@-webkit-keyframes run 
    0% { left: 0;}
    50%{ left : 100%;}
    100%{ left: 0;}


</style>
