<template>
   <header id="header">
    <img src="https://cdn-icons-png.flaticon.com/128/149/149145.png" id="logo" @click="telaOpcoes()">
    <nav id="nav">
       <button id="botao-mobile"></button>
          <span id="hamburguer"></span>
       <ul id="menu">
         <li><a href="/">Perfil</a></li>
         <li><a href="/">Redes Mapeadas</a></li>
         <li><a href="/">Redes online</a></li>
         <li><a href="/">Profissionais</a></li>
         <li><a href="/">Mais informações</a></li>
         <li><a href="/">Configurações</a></li>
       </ul>
     </nav>
  
   </header>
   
</template>


<script> 
export default {
    name: 'TelaMenuPage',
    methods:{
      telaOpcoes(){
            this.$router.push("opcoes");
      }
        }
    }

</script>


<style>
body, ul {
  margin: 0px;
  padding: 0px;
}

a {
  color: black;
  text-decoration: none;
  font-family: sans-serif;
}

a:hover{
  background: #f48b9b;
}

#logo{
  padding-top: 5px;
  width: 35px;
  height: 35px;
}

#header{
  box-sizing: border-box;
  height: 70px;
  padding: 1rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: #f1a4ae;
}

#menu{
  display: flex;
  list-style: none;
  gap: 0.5rem;
}

#menu a{
  display: block;
  padding: .5rem;
}

#botao-mobile{
  display: none;
}
.logo-principal{
  display: block;
  margin: 0 auto;
  width: 300px;
  height: 300px;
  margin-top: 150px;
}
.botao-principal{
  width: 70px;
  height: 70px;
  background-color: #fd8ca0;
  border: 1px #f88ea0;
  border-radius: 100%;
  margin: 0 auto;
  color: white;
  display: block;
  padding: 10px;
  margin-top: 50px;
}

@media (max-width: 600px){
  #botao-mobile {
    display: block;
  }
  #menu{
    display: block;
    position: absolute;
    width: 70%;
    top: 70px;
    right: 0px;
    background: #f1a4ae;
    height: 0px;
    visibility: hidden;
    overflow: hidden;
    transition: 0.6s;
    z-index: 1000;
    
  }
  #nav.active #menu {
    height: calc(100vh - 70px);
    visibility: visible;
    overflow: auto;
  }
  #menu a {
    padding: 1.5rem 0;
    margin: 0 1rem;
    border-bottom: 3px solid #f2788b;
  }
  #botao-mobile{
    display: flex;
    padding: .5rem  1rem;
    font-size: 1rem;
    border: none;
    background: none;
    cursor: pointer;
    gap: 0.5rem;
  }
  #hamburguer{
    display: block;
    width: 20px;
    border-top: 2px solid;
    color: white;
  }
  #hamburguer::after, #hamburguer::before{
    content: '';
    width: 20px;
    height: 2px;
    display: block;
    background: white;
    margin-top: 5px;
    transition: 0.3s;
    position: relative;
  }
  #nav.active #hamburguer{
    border-top-color: transparent;
  }
  #nav.active #hamburguer::before{
    transform: rotate(135deg);
  }
   #nav.active #hamburguer::after{
    transform: rotate(-135deg);
    top: -7px;
  }
}
</style>