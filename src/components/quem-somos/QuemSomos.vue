<template>
  <div class="container">
    <img class="background" src="@/assets/faixa.svg" alt="">
    <div class="who-we-are-wrapper">
      <div class="title">
        <h1>Quem somos</h1>
      </div>
      <!-- <Descricao/> -->
      <div class="description">
        <div class="carousel-wrapper">
          <carousel class="carousel"
            autoplay="true"
            autoplayTimeout="3000"
            perPage="1"
            paginationColor="#FFF"
            paginationActiveColor="#CCC"
            loop="true"
            >
            <slide class="slide">
              <img src="@/assets/img1.jpeg" alt="Inauguração DevAcademy">
            </slide>
            <slide class="slide">
              <img src="@/assets/img2.jpeg" alt="Inauguração DevAcademy">
            </slide>
            <slide class="slide">
              <img src="@/assets/img3.jpeg" alt="Inauguração DevAcademy">
            </slide>
            <slide class="slide">
              <img src="@/assets/img4.jpeg" alt="Inauguração DevAcademy">
            </slide>
          </carousel>
        </div>
        <div class="text-content">
          <p>Nós somos um projeto de desenvolvimento criado pela <strong>Casa Magalhães</strong> para fomentar o desenvolvimento de talentos em tecnologias que são usadas na empresa em prol do crescimento consistente das nossas soluções.</p>
          <p>O objetivo do projeto é de trazer para o nosso meio, mentes inquietas por conhecimento, apaixonadas por tecnologia e dispostas a fazer parte dessa transformação. Atualmente temos um núcleo instalado em <strong>Quixadá</strong>, em parceria com o campus da <strong>UFC</strong> na cidade.</p>
          <p>No dia 09/03/2020 aconteceu a inauguração oficial do ambiente onde nossos Dev'ers irão atuar.</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// import Descricao from './components/Descricao.vue';
import { Carousel, Slide } from 'vue-carousel';

export default {
  name: 'Descricao',
  components: {
    // Descricao
    Carousel,
    Slide
  }
}
</script>

<style lang="stylus" scoped>
.container
  display flex
  box-sizing border-box

.background
  width 100%
  display none

.who-we-are-wrapper
  display flex
  position absolute
  flex-direction column
  padding 0 5px
  box-sizing border-box
  width 100%
  background-color #dcb216

.title
  color #FFF

  h1
    font-size 40px

.description
  display flex
  flex-direction column
  padding-bottom 20px

.carousel-wrapper
  display flex
  justify-content center

.carousel
  display flex
  justify-content center
  width 100%

.slide
  display flex
  justify-content center

  img
    width 95vw
    max-width 540px
    border-radius 10px

.text-content
  display flex
  flex-direction column
  justify-content flex-start
  text-align justify
  font-size 24px
  padding 0 10px
  color #FFF

  p
    margin 20px 0
  
@media screen and (min-width: 600px)
  .who-we-are-wrapper
    padding 0 10px

@media screen and (min-width: 1200px)
  .container
    align-items center

  .who-we-are-wrapper
    margin 0 10%
    background none
  
  .background
    display block 

  .carousel
    width 640px

  .description
    flex-direction row

  .img
    img
      max-height 480px
  
  .text-content
    width calc(80% - 640px)
    padding-left 30px
</style>