<template>
 <v-app id="about">
  <NavBar />
  <v-container fluid>
   <div class="head">
    <v-row>
     <v-col cols="12" sm="6" md="5">
      <div style="position: relative" class="mt-16" id="name">
       <div class="name-container">
        <h1 class="text-grey inline">Olá, eu sou</h1>
        <h1 class="text-grey inline">Hugo Ferreira</h1>
        <div class="subtext text-grey">
         Estudante de programação com foco em Back-End
        </div>
       </div>
       <v-btn
        tile
        dark
        class="text-purple mt-8"
        variant="outlined"
        href="https://api.whatsapp.com/send/?phone=%2B5527988737883&text&type=phone_number&app_absent=0"
        target="_blank"
       >
        Contato
       </v-btn>
      </div>
     </v-col>
     <v-col cols="12" sm="6" md="2">
      <div
       style="
        position: absolute;
        z-index: 9999;
        bottom: 15px;
        margin-left: auto;
        margin-right: auto;
        left: 0;
        right: 0;
        text-align: center;
       "
      >
       <v-icon>fas fa-angle-double-down</v-icon>
      </div>
     </v-col>
     <v-col cols="12" md="5"></v-col>
    </v-row>
   </div>
   <v-col cols="12" class="mt-16" id="sobre">
    <div>
     <v-row>
      <v-col cols="12" sm="6">
       <div class="circulo">
        <v-img
         src="../assets/foto.jpeg"
         alt="minha imagem"
         class="img-responsive-circulo"
        ></v-img>
       </div>
      </v-col>
      <v-col cols="12" sm="6">
       <h5 class="mt-16">Sobre mim</h5>
       <div style="width: 120px"></div>
       <h4 class="mt-n4">Entusiasta em tecnologia</h4>
       <h4>Desenvolvedor com foco em Back-End</h4>
       <p class="text-black">
        Meu nome é Hugo da Cruz Ferreira, tenho 20 anos, curso TADS na faculdade
        UNISALES aonde atualmente estou no 4 período. Estou sempre buscando
        aprender novas tecnologias e formas de aprimorar mais meu conhecimento.
        Curso atualmente tecnólogo com duração de 2.5 anos e meio mas tenho
        planos futuros de prosseguir e alcançar o mestrado em I.A.
       </p>
       <br />
       <p class="text-black">
        Tive interesse em tecnologia por influência familiar, especificamente
        meus irmãos mais velhos, por sempre gostarem de vídeo-game e me
        incentivarem a jogar junto deles. Desta forma, de acordo com meu
        crescimento fui me interessando pelo mundo dos jogos, até conseguir ter
        acesso livre a internet, e me criar novos interesses como criação de
        sites e aplicativos para diversas plataformas, não mais focando somente
        em jogos para consoles.
       </p>
       <br />
       <p class="text-black">
        Atualmente tenho alguns hobbies, que são andar de skate e jogar com os
        amigos. Geralmente alterno as atividades no fim de semana, ou até mesmo
        encaixo algum tempo no fim de semana. Atualmente trabalho em uma empresa
        de transportes rodoviários, atuando na minha segunda formação na área de
        logística. Busco oportunidade no mercado de T.I para estágio ou vaga
        para junior.
       </p>
      </v-col>
     </v-row>
    </div>
   </v-col>
  </v-container>

  <div id="footer-contatos">
   <v-btn
    icon
    color="black"
    class="text-white mr-2"
    href="https://github.com/hugo-exe"
    target="_blank"
   >
    <v-icon class="fab fa-github"></v-icon>
   </v-btn>
   <v-btn
    icon
    color="black"
    class="text-white mr-2"
    href="https://www.linkedin.com/in/hugo-ferreira-98aaa6237/"
    target="_blank"
   >
    <v-icon class="fab fa-linkedin"></v-icon>
   </v-btn>
   <v-btn
    icon
    color="black"
    class="text-white mr-2"
    href="mailto:hugodacruzferreira1@gmail.com"
    target="_blank"
   >
    <v-icon class="fas fa-envelope"></v-icon>
   </v-btn>
  </div>
 </v-app>
</template>

<script>
import { defineComponent } from "vue";

// Components
import NavBar from "@/components/NavBar.vue";

export default defineComponent({
 name: "AboutView",
 components: {
  NavBar,
 },
});
</script>

<style scoped>
.v-container {
 padding: 16px 0;
}
.head {
 position: relative;
 text-align: center;
 padding: 12px;
 margin-bottom: 6px;
 height: 400px;
 width: 100%;
 color: white;
}
.head::before {
 content: " ";
 position: absolute;
 top: 0;
 left: 0;
 height: 100%;
 width: 100%;
 background: black;
 transform: skew(0deg, 0deg);
}

.circulo {
 justify-content: center;
 display: block;
 margin-left: auto;
 margin-right: auto;
 width: 70%;
 max-width: 300px;
 height: auto;
 background-color: white;
 border-radius: 50%;
 overflow: hidden;
}
.mt-16 {
 padding-bottom: 16px;
}
#footer-contatos {
 height: 50px;
 position: fixed;
 bottom: 0;
 left: 0;
 width: 100%;
 background-color: #000000;
 padding: 10px 0;
 text-align: center;
 z-index: 1000;
}
.v-container {
 padding: 16px 0;
 padding-bottom: 60px;
}

.inline {
 display: inline;
}

.name-container {
 display: flex;
 flex-direction: column;
 align-items: center;
 justify-content: center;
 height: 100%;
}

@media screen and (max-width: 600px) {
 .circulo {
  width: 80%;
  max-width: 250px;
  margin: 20px auto;
  position: relative;
  overflow: hidden;
  border-radius: 50%;
  box-shadow: 0 0 0 5px rgb(255, 255, 255), 0 0 0 8px rgb(255, 255, 255);
 }

 .img-responsive-circulo {
  width: 100%;
  height: 100%;
  object-fit: cover;
  position: absolute;
  top: 0;
  left: 0;
  border-radius: 50%;
 }
}

@media screen and (max-width: 600px) {
 .inline {
  display: block;
  font-size: 1.5rem;
  margin: 0;
 }

 .subtext {
  margin-top: 4px;
  font-size: 0.9rem;
 }
 .head {
  height: auto;
 }
 .circulo {
  width: 200px;
  height: 200px;
 }
 .mt-16 {
  padding-bottom: 16px;
 }
 #footer-contatos {
  height: 60px;
 }
}
</style>
