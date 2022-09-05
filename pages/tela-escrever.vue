<template>
  <div>
    <span>Escreva aqui sua história:</span>
    <p style="white-space: pre-line">{{ message }}</p>
   
    <textarea v-model="message" placeholder="Relate seu depoimento!"></textarea><br>
  </div>
</template>
<script></script>
<style>
body {
  background-color: #f8d4d4;
}
div {
  padding-top: 100px;
  display: flex;
  flex: center;
  padding-left: 130px;
  padding-right: 130px;
}

.botao {
  width: 40%;
  height: 40%;
  background-color: #fd8ca0;
  border: 1px #f88ea0;
  border-radius: 6px;
  margin: 0 auto;
  color: white;
  padding: 10px;
  margin-top: 15px !important;
}
</style>
