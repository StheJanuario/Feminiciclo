<template>
    <div>
      <img src="logo.png" class="logo" />
      <p>Gostaria de acessar como:</p>
      <NuxtLink to="/tela-vitima"
        ><b-button class="botao">VÍTIMA</b-button></NuxtLink
      >
      <NuxtLink to="/tela-profissional"
        ><b-button class="botao">PROFISSIONAL</b-button></NuxtLink
      >
      <NuxtLink to="/tela-instituicao"
        ><b-button class="botao">INSTITUIÇÃO</b-button></NuxtLink
      >
    </div>
  </template>
  
  <script>
  export default {
    name: 'IndexPage'
  }
  </script>
  <style>
  html,body {
    height: 100%;
    width: 100;
    background-color: #f8d4d4;
  }
  .logo {
    display: block;
    margin: 0 auto;
    width: 250px;
    height: 250px;
    margin-top: 25px;
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
    margin-top: 15px !important;
  }
  p {
    text-align: center !important;
    font-size: 30px !important;
    margin: 0 auto;
    margin-top: 75px;
  }
  </style>