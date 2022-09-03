<template>
  <div>
    <img src="logo.png" class="logo">
      <b-button class="botao" @click="telaMenu()">SEJA BEM-VINDA</b-button>
  </div>

</template>

<script>
export default {
     name: 'TelaEntrarPage',
     methods:{
      telaMenu(){
        this.$router.push("tela-menu")
      }
     }
}
</script>

<style>
html,
body {
  height: 100%;
  width: 100;
  background-color: #f8d4d4;
}

.logo {
  display: block;
  margin: 0 auto;
  width: 300px;
  height: 300px;
  margin-top: 250px;
}

.botao {
  width: 15%;
  height: 20%;
  background-color: #fd8ca0;
  border: 1px #f88ea0;
  border-radius: 3px;
  margin: 0 auto;
  color: white;
  display: block;
  padding: 10px;
  margin-top: 70px;
}
</style>