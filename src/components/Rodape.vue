<template>
  <div class="footer">
    <div class="content">
      <div class="left">
        <h2 class="title">Dev Academy</h2>
        <p>
          Endereço: R. Basílio Emiliano Pinto, 427 - Centro, Quixadá - CE, 63900-211 <br />
          Telefone: (88) 9999-9999
        </p>
      </div>
      <div class="right">
        <h2 class="title">Powered by</h2>
        <a href="https://www.casamagalhaes.com.br/" target="_blank">
          <img src="../assets/cm-logo.png" />
        </a>
      </div>
    </div>
      <div class="copy">
        <span>
          &copy; 2020 Copyright:
        </span>
        <a href="http://devacademy.netlify.com/" target="_blank"> devacademy.com.br </a>
      </div>
  </div>
</template>

<script>
export default {
  name: 'Footer'
};
</script>

<style lang="stylus" scoped>
.footer
  position relative
  color white
  z-index 2
  width 60%
  margin-left auto
  margin-right auto
  

.left
  float left

.right
  float right

.copy
  position relative
  margin-left auto
  margin-right auto
  z-index 2
  text-align center
  margin-bottom 10px
  margin-top 10px

.content 
  width 50vw  
  display inline-block

h2
  font-weight: bold;

a
  color white
  text-decoration none;


a:visited
  color white
  text-decoration none;


a:hover
  color white
  text-decoration: underline;

img
  z-index 2
  height: 70px;
  width: 90px
</style>
