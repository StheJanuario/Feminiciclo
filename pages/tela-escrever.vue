<template>
  <div id="area">
    <form id="formulario" autocomplete="off">
      <fieldset>
        <div id="perfilUsuaria">
          <img src="perfil.png" width="50px" height="50px" />
          <legend>Perfil Usuária</legend>
        </div>
        <br />
        <label>Escreva aqui seu Feedback:</label><br /><textarea
          class="msg"
          cols="50"
          rows="10"
          v-model="form.descricao"
        ></textarea
        ><br />
        <div id="botoes">
          <button v-on:click.prevent = "enviarFeedback" class="botao" type="submit" value="Enviar">Enviar</button>
        </div>
      </fieldset>
      <NuxtLink to="/tela-feedbacks"></NuxtLink>
    </form>
  </div>
</template>

<script>
export default {
  data(){
    return {
      form: {
        descricao: "",
      },
      show: true,      
    }
  },
  methods:{
    async enviarFeedback({ $axios }) {
     const response = await this.$axios.post("/feedback", {
        descricao: this.form.descricao,
      }
     )
     if(response.status == 200){
      alert(
        "Feedback enviado com sucesso"
      )
      this.$router.push("/tela-feedbacks");
     }else{
      alert(
        `Erro: ${response.status}`
      )
     }
    },

  excluirFeedback({$axios}){
    this.$axios.delete('/feedbacks/delete/{id}');
    const result = document.getElementById("deletar");
    result.innerHTML = "feedback excluído com sucesso";
  }
      
    }
  }
</script>
<style>
body{
  height: 100%;
  width: 100;
  background-color: #f8d4d4;
}
#area {
  position: relative;
  left: 37%;
  top: 29%;
  width: 320px;
  height: 270px;
  padding-top: 50px;
}
#area #formulario {
  position: absolute;
  display: block;
}
#perfilUsuaria {
  display: flex;
}
#botoes{
  display: flex;
}
.botao {
  width: 120px;
  height: 35px;
  background-color: #fd8ca0;
  border: 1px #f88ea0;
  border-radius: 3px;
  margin: 0 20px 0 20px;
  color: white;
  margin-top: 20px !important;
}

fieldset {
  width: 300px;
  height: 250px;
}
legend {
  font-style: bold;
}
#formulario label {
  position: absolute;
  left: 19px;
  margin-right: 5px;
}
</style>
