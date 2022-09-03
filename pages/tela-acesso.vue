<template>
  <b-container>
   <h1>Vítima</h1>
   <p>Informações necessárias</p>
  
   <label>Idade</label>
   <b-form-input placeholder=" Ex 20 anos"></b-form-input>
   <label>RG</label>
   <b-form-input placeholder="Ex: XX.XXX.XXX.X"></b-form-input>
   <label>Boletim de Ocorrência</label>
   <b-form-input placeholder="Foi feito um boletim de Ocorrência ? (Sim) ou (Não)"></b-form-input>
   <label>Corpo de Delito</label>
   <b-form-input placeholder="Ouve exame de corpo de delito ? (Sim) ou (Não)"></b-form-input>
  <b-button class="botao" @click="telaEntrar()">PRÓXIMO</b-button>
  </b-container>
  
</template>

<script>
export default {
 name: 'TelaAcessoPage',
 methods:{
  telaEntrar(){
    this.$router.push("tela-entrar")
  }
 }
}
</script>

<style  scoped>
html, body{
 height: 100%;
 width: 100;
 background-color:#f8d4d4;

}

.botao{
  width: 15%;
  height: 20%;
  background-color: #fd8ca0;
  border: 1px #f88ea0;
  border-radius: 3px;
  margin: 0 auto;
  color: white;
  display: block;
  padding: 10px;
  margin-top: 20px;
}
h1{
  font-size: 50px;
}
p{
  font-size: 18px;
  text-align: left !important;
  margin-top: 3px;
}
.input{
  font-size:20px;
}
</style>