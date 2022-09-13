<template>
  <b-container>
   <h1>Instituição</h1>
   <p>Informações Necessárias</p>
  
   <label>Nome:</label>
   <b-form-input placeholder="Digite o nome da instituição/Rede de Apoio."></b-form-input>
   <label>Endereço:</label>
   <b-form-input placeholder="Ex: Rua das Flores,458."></b-form-input>
   <label>CNPJ:</label>
   <b-form-input placeholder="Digite o CNPJ da instituição (se houver)."></b-form-input>
   <label>Tipo de apoio:</label>
   <b-form-input placeholder="Descrição do tipo de apoio fornecido para as mulheres."></b-form-input>
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