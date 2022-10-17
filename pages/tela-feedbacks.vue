<template>
    <div id="principal"><br>
        <p>FEEDBACKS:</p>
        <div v-bind:key ="feedback.id" v-for="feedback in feedbacks">
          {{feedbacks.id}}- {{feedback.descricao}}
        <button v-on:click.prevent = "excluirFeedback(feedback.id)" class="botao" type="submit" value="Enviar">Excluir</button>
        </div>
    </div>
</template>

<script>
  export default {
    async asyncData({$axios}){
      const resposta = await $axios.get("/feedback");
      const feedbacks = resposta.data;
      console.log(feedbacks);
      return {feedbacks};
    },
    methods:{
      async excluirFeedback(feedbackId){
      const result = await this.$axios.delete(`/feedback/${feedbackId}`);
      if(result){
        alert("Delete realizado com sucesso");
      }else{
        alert("Não foi possível realizar o delete");
      }
      }
    }
  }
</script>
<style>
#principal{
  box-sizing: border-box;
  background-color: pink;
  height: 100%;
  width: 35%;
  display: block;
  margin: 0 auto;
  margin-top: 18%;
  border-radius: 15px;
}
.botao{
  margin-left: 88%;
}
</style>