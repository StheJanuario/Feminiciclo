<template>
  <div id="principal">

    <div>
      <header id="header">
        <img src="https://cdn-icons-png.flaticon.com/128/149/149145.png" id="logo" @click="telaOpcoes()">
        <nav id="nav">
          <span id="hamburguer"></span>
          <ul id="menu">
            <li><button id="botao-mobile"></button></li>
            <li><a href="">Perfil</a></li>
            <li><NuxtLink to="/mapeamento">Instituições Mapeadas</NuxtLink></li>
            <li><a href="">Mais informações</a></li>
            <li><a href="">Configurações</a></li>
          </ul>
        </nav>
      </header>
    </div>

    <div id="componentes">
      <img src="logo.png" class="logo-principal"><br>
      <img src="IconeSocorro.png" class="botao-socorro" id="resposta" v-on:click="alertarSocorro()">
    </div>
    
    <footer class="rodape">
      <section class="cabecalho">

      <div class=informações-rodapé>
        <h3>Inicio</h3>
        <p>Home</p>
        <p>Chat</p>
        <p>Telefone</p>
      </div>

      <div class=informações-rodapé>
        <h3>Sobre nós</h3>
        <p>Informações do Site</p>
        <p>Contato</p>
        <p>Mais</p>
      </div>

      <div class=informações-rodapé>
        <h3>Suporte</h3>
        <p>Ligue 190 - PM</p>
        <p>Ligue 197 - Disque Denúncia </p>
        <p>Ligue 180 - Central de Atendimento a mulher</p>
      </div>

      <div class=informações-rodapé>
      <img src="Icones-rodape.jpeg">
      </div>

    </section>
    </footer>
  </div>
</template>


<script>
export default {
  name: 'TelaMenuPage',
  methods: {
    telaOpcoes() {
      this.$router.push("opcoes");
    },
    alertarSocorro(){
    alert("Chamando a polícia (190)...");
}
  }
}

</script>


<style>
body,
ul {
  margin: 0px;
  padding: 0px;
}
#principal{
  background-color: #f8d4d4;
}
a {
  color: black;
  text-decoration: none;
  font-family: sans-serif;
}


a:hover {
  background: #f48b9b;
}

#logo {
  padding-top: 5px;
  width: 35px;
  height: 35px;
}

#header {
  box-sizing: border-box;
  height: 70px;
  padding: 1rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: #f1a4ae;
}
#menu {
  display: flex;
  list-style: none;
  gap: 0.5rem;
}

#menu a {
  display: block;
  padding: .5rem;
}

#botao-mobile {
  display: none;
}

.logo-principal {
  display: block;
  margin: 0 auto;
  width: 200px;
  height: 200px;
  margin-top: 150px;
}
.botao-socorro{
  display: block;
  margin: 0 auto;
  width: 80px;
  height: 80px;
}

.botao-principal {
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
.rodape{
  background-color: white;
  font-family: 'Sarala', sans-serif;
  color: rgb(55, 53, 53);
  height: 15px;;
  font-size: 16px;
  margin-top: 30px;
}
.cabecalho {
  margin-top: 100px;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-around;
  padding: 18px;
}
.informacoes-rodape{
  display: flex;
  flex-direction: collumn;
}
#componentes{
  height: 90%;
}

@media (max-width: 600px) {
  #botao-mobile {
    display: block;
  }

  #menu {
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

  #botao-mobile {
    display: flex;
    padding: .5rem 1rem;
    font-size: 1rem;
    border: none;
    background: none;
    cursor: pointer;
    gap: 0.5rem;
  }

  #hamburguer {
    display: block;
    width: 20px;
    border-top: 2px solid;
    color: white;
  }

  #hamburguer::after,
  #hamburguer::before {
    content: '';
    width: 20px;
    height: 2px;
    display: block;
    background: white;
    margin-top: 5px;
    transition: 0.3s;
    position: relative;
  }

  #nav.active #hamburguer {
    border-top-color: transparent;
  }

  #nav.active #hamburguer::before {
    transform: rotate(135deg);
  }

  #nav.active #hamburguer::after {
    transform: rotate(-135deg);
    top: -7px;
  }
}
</style>