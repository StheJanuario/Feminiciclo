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
        ></textarea
        ><br />
        <div id="botoes">
          <input class="botao" type="submit" value="Excluir" />
          <input class="botao" type="submit" value="Enviar" />
        </div>
      </fieldset>
    </form>
  </div>
</template>

<script>
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
  align-items: center;
}
.botao {
  width: 80%;
  height: 60%;
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
