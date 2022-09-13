<template>
  <b-container>
   <h1>Profissional</h1>
   <p>Informações necessárias</p>
  
   <label>CPF:</label>
   <b-form-input placeholder="Ex: XXX.XXX.XXX-XX."></b-form-input>
   <label>Área de Formação:</label>
   <b-form-input placeholder="Digite a área em que você trabalha."></b-form-input>
   <label>Horário de Atendimento:</label>
   <b-form-input placeholder="Digite seu horário de Atendimento."></b-form-input>
   <label>Forma de Atendimento:</label>
   <b-form-input placeholder="Qual a forma de atendimento? (on-line) ou (presencial)."></b-form-input>
  <b-button class="botao" @click="telaEntrar()">REGISTRAR</b-button>
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