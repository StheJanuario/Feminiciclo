<template>
  <div >
    <div>
      <p>feedbacks publicos</p>
      <img src="feedbacksPublicoIcone.png" @click="irParaFeedbacks()" />
    </div>
    <div>
      <p>Escrever</p>
      <img src="iconeEscrever.png" @click="irParaEscrever()" />
    </div>
  </div>
</template>

<script>
export default {
    name: 'TelaOpcoes',
    methods:{
        irParaEscrever(){
            this.$router.push("tela-escrever");
            
        },  
        irParaFeedbacks(){
            this.$router.push("tela-feedbacks");
            
        }
    }
}
</script>
<style>
body {
  background-color: #f8d4d4;
 
}
div{
  padding-top: 100px;
  display:flex;
  flex: center;
  padding-left: 130px;
  padding-right: 130px;
}
</style>
