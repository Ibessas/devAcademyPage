<template>
  <!-- Footer -->
  <mdb-footer id="footer" color="#303030" z-index="2" class="font-small pt-4 mt-4">
    <mdb-container class="text-left">
      <mdb-row>
        <mdb-col sm="6">
          <h5 class="title">Dev Academy</h5>
          <p>Endereço: R. Basílio Emiliano Pinto, 427 - Centro, Quixadá - CE, 63900-211 <br> 
            Telefone: (88) 9999-9999
          </p>
        </mdb-col>
        <mdb-col sm="6">
          <h5 class="title">Links</h5>
          <ul>
            <li  class="list-unstyled">
                <a  href="https://www.casamagalhaes.com.br/">
                    <img id="imagem" src="../assets/cm-logo.png">
                </a>
                </li>
          </ul>
        </mdb-col>
      </mdb-row>
    </mdb-container>
    <div class="footer-copyright text-center py-3">
      <mdb-container fluid>
        &copy; 2020 Copyright: <a href="http://devacademy.netlify.com/"> devacademy.com.br </a>
      </mdb-container>
    </div>
  </mdb-footer>
  <!-- Footer -->
</template>

<script>
  import { mdbFooter, mdbContainer, mdbRow, mdbCol } from 'mdbvue';

  export default {
    name: 'FooterPage',
    components: {
      mdbFooter,
      mdbContainer,
      mdbRow,
      mdbCol
    }
  }
</script>

<style lang="stylus" scoped>
    #imagem {
        height: 70px;
        width: 90px
    }

    #footer {
        margin-top: 200px;
    }
</style>

