<template>
  <div>
    <img src="perfil.png" class="perfil">
    <h1>Seja Bem-Vinda</h1>
    <b-container>
      <label>Nome</label>
      <b-form-input placeholder=" Amanda Tavares da Silva"></b-form-input>
      <label>Idade</label>
      <b-form-input placeholder="31 anos"></b-form-input>
      <label>CPF</label>
      <b-form-input placeholder="000.111.222/33"></b-form-input>
      <label>Endereço</label>
      <b-form-input placeholder="Rua das Flores, 456."></b-form-input>
      <div class="btn_form">
        <!-- <NuxtLink to="/"> <b-button class="botao">Alterar dados</b-button></NuxtLink> -->
        <b-button class="botao" @click="irParaIndex()">Alterar dados</b-button>
         <!-- <NuxtLink to="/"> <b-button class="botao">Prosseguir</b-button></NuxtLink> -->
        <b-button class="botao" @click="telaCadastro()">Prosseguir</b-button>
      </div>
    </b-container>
  </div>
</template>

<script>
export default {
    name: 'TelaInicialPage',
    methods:{
        irParaIndex(){
            this.$router.push("/");
            
        },  
        telaCadastro(){
            this.$router.push("tela-entrar");
            
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

.botao {
  max-width: 15%;
  max-height: 50px;
  background-color: #fd8ca0;
  border: 1px #f88ea0;
  border-radius: 3px;
  margin: 0 20px 0 20px;
  color: white;
  /* flex-direction: row !important; */
  padding: 10px;
  margin-top: 20px !important;
  display: inline-block;
}

.btn_form{
    display: flex;
    justify-content: center;
}

h1{
   text-align: center;
   font-size: 25px;
   margin-top:15px;
}

.perfil{
    display: block;
  margin: 0 auto;
  width: 100px;
  height: 100px;
}

</style>