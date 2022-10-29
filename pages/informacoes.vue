<template>
    <section class="conteudo">
        <section class="conteudo-principal">
            <div class="conteudo-principal-escrito">
                <section class="informações">
                    <h1 class="conteudo-principal-escrito-titulo">VOCÊ NÃO ESTÁ SOZINHA!</h1>
                    <p class="conteudo-principal-escrito-subtitulo">As mulheres que sofrem violência não falam sobre o
                        problema por um misto de sentimentos: vergonha, medo, constrangimento.
                        Os agressores, por sua vez, não raro, constroem uma autoimagem de parceiros perfeitos e bons
                        pais, dificultando a revelação da violência pela mulher.
                        Quando a vítima silencia diante da violência, o agressor não se sente responsabilizado pelos
                        seus atos – isso sem contar o fato de que a sociedade, em suas diversas práticas, reforça a
                        cultura patriarcal e machista, o que dificulta a percepção da mulher de que está vivenciando o
                        ciclo da violência.
                        <br>
                        Portanto, pensando neste assunto tão delicado e sério resolvemos criar um aplicativo de ajuda
                        para essas vítimas que visa ajudar a sair do ciclo violento em que vivem dando suporte
                        psicológico para as mesmas além de mapeamento de redes de apoio e um botão de socorro imediato.
                        Aos poucos com ajuda da tecnologia iremos mudar este quadro!<br>
                        <br>
                    <strong class="titulos">Desenvolvedoras:</strong><br>
                        Ágatha Rizzo Cezar<br>
                        Emanoelle Cardoso Vieira<br>
                        Larissa Vitória Rodrigues Ribeiro<br>
                        Stefanye Januário dos Santos
                    </p>
                </section>
            </div>
        </section>

        <section class="conteudo-secundario">
            <h3 class="conteudo-secundario-titulo">O que faremos por você?</h3><br>

            <section class=cabecalho-menu>
                <div>
                    <img class="conteudo-principal-imagem" src="imagemProfissionais.png"
                        alt="Imagem de profissionais">
                    <p class="titulo-imagens">AJUDA DE PROFISSIONAIS</p>
                </div>

                <div>
                    <img class="conteudo-principal-imagem" src="Mulher.jpg" alt="Imagem mulher com megafone">
                    <p class="titulo-imagens">UM BOTÃO DE SOCORRO PARA <br> QUANDO ESTIVER EM PERIGO</p>
                </div>

                <div>
                    <img class="conteudo-principal-imagem" src="imagemApoio.jpg" alt="Imagem de apoio">
                    <p class="titulo-imagens">REDES/INSTITUIÇÕES DE APOIO</p>
                </div>
            </section>
        </section>
    </section>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Libre+Baskerville&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Quicksand:wght@300&display=swap');

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  text-decoration: none;
  background-color: #f8d4d4;
  font-family: 'Quicksand', sans-serif;
}
.conteudo {
  margin-bottom: 48px;
  border-top: 0.4px solid #FFF2E7;
}

.conteudo-principal {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-around;
}
.conteudo-principal-escrito {
  display: flex;
  flex-direction: column;
  gap: 32px;
}

.conteudo-principal-escrito-titulo {
  padding-top: 25px;
  font-weight: 400;
  font-size: 40px;
  color: #f7f7f7;
  text-align:center;
  font-family: 'Libre Baskerville', serif;
}

.conteudo-principal-escrito-subtitulo {
  font-size: 20px;
  color: black;
  text-align: center;
}
.titulos{
  color: white;
  font-family:'Libre Baskerville';
}
.conteudo-secundario {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 15px;
  margin-top: 48px;
}

.conteudo-secundario-titulo {
  border-top: 0.4px solid #FFF2E7;
  padding-top: 48px;
  font-family: 'Libre Baskerville', serif ;
  font-weight: 400;
  font-size: 24px;
  color: white;
  margin-bottom: 16px;
}
.cabecalho-menu {
  display: flex;
  gap: 35px;
}
.conteudo-principal-imagem {
  height: 300px;
  padding-top: 2px;  
  border-radius: 60px;
}
.titulo-imagens{
  text-align: center;
}
</style>