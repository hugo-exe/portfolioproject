<template>
 <v-app id="home">
  <NavBar />
  <v-container fluid>
   <div class="head">
    <v-row>
      <v-col cols="12" sm="6" md="5">
            <div style="position: relative" class="mt-16" id="name">
        <div class="name-container">
          <h1 class="text-grey inline">Olá, eu sou </h1>
          <h1 class="text-grey inline">Hugo Ferreira</h1>
          <div class="subtext text-grey">Estudante de programação com foco em Back-End</div>
        </div>
       <v-btn
        tile
        dark
        class="text-purple mt-8"
        variant="outlined"
        href="https://api.whatsapp.com/send/?phone=%2B5527988737883&text&type=phone_number&app_absent=0"
        target="_blank"
        >Contato</v-btn
       >
      </div>
     </v-col>
     <v-col cols="2">
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
     <v-col cols="5"></v-col>
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
       <p class="text-grey">
        Bem-vindo ao meu portfolio! Sou apaixonado por tecnologia e programação. Aqui compartilho um pouco do que aprendo e desenvolvo. Fique à vontade para explorar e conhecer mais sobre meu trabalho e projetos.

       </p>
       <br />
       <p class="text-grey">
        Obrigado por visitar! Se você tiver alguma pergunta ou quiser iniciar um projeto, não hesite em entrar em contato comigo.
       </p>
      </v-col>
     </v-row>
    </div>
   </v-col>
   <div class="text-center mt-4">
    <h2>Minhas especialidades</h2>
    <div style="width: 120px; margin: 0 auto"></div>
   </div>
   <v-col cols="12" class="p1" id="portfolio">
    <div class="grid-container">

     <div class="child">
      <div class="icons-frontend">
       <v-btn icon color="black" class="text-white mr-2">
        <v-icon class="fab fa-html5"></v-icon>
       </v-btn>
       <v-btn icon color="black" class="text-white mr-2">
        <v-icon class="fab fa-css3"></v-icon>
       </v-btn>
       <v-btn icon color="black" class="text-white mr-2">
        <v-icon class="fab fa-js"></v-icon>
       </v-btn>
       <v-btn icon color="black" class="text-white mr-2">
        <v-icon class="fab fa-react"></v-icon>
       </v-btn>
       <v-btn icon color="black" class="text-white mr-2">
        <v-icon class="fab fa-vuejs"></v-icon>
       </v-btn>
      </div>
      <h3 class="ml-3 mt-4">Front-End</h3>
      <p class="text-grey ml-3 mt-4 text-caption">
       Como estudante de programação, estou sempre aprendendo e explorando as
       últimas tecnologias Front-End. Meu foco é criar interfaces intuitivas e
       responsivas, combinando design e funcionalidade para oferecer a melhor
       experiência ao usuário.
      </p>
     </div>


     <div class="child">
      <div class="icons-backend">
       <v-btn icon color="black" class="text-white mr-2">
        <v-icon class="fab fa-java"></v-icon>
       </v-btn>
       <v-btn icon color="black" class="text-white mr-2">
        <v-icon class="fab fa-python"></v-icon>
       </v-btn>
       <v-btn icon color="black" class="text-white mr-2">
        <v-icon class="fab fa-node"></v-icon>
       </v-btn>
      </div>
      <h3 class="ml-3 mt-4">Back-End</h3>
      <p class="text-grey ml-3 mt-4 text-caption">
       Como estudante de programação, estou aprimorando minhas habilidades em
       desenvolvimento Back-End para criar sistemas robustos e eficientes que
       suportem aplicações escaláveis e seguras.
      </p>
     </div>
    </div>
   </v-col>
  </v-container>
  <div id="footer-contatos">
    <v-btn icon color="black" class="text-white mr-2" href="https://github.com/hugo-exe" target="_blank">
      <v-icon class="fab fa-github"></v-icon>
    </v-btn>
    <v-btn icon color="black" class="text-white mr-2" href="https://www.linkedin.com/in/hugo-ferreira-98aaa6237/" target="_blank">
      <v-icon class="fab fa-linkedin"></v-icon>
    </v-btn>
    <v-btn icon color="black" class="text-white mr-2" href="mailto:hugodacruzferreira1@gmail.com" target="_blank">
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
 name: "HomeView",
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
 padding-bottom: 15px;
 text-align: center;
}
.child {
 display: inline-block;
 padding: 2rem 1rem;
 text-align: center;
}
.imgHover {
 padding: 0 200px;
}

.icons-frontend,
.icons-backend {
 text-align: center;
 margin-bottom: 10px; 
}
.grid-container {
 display: grid;
 grid-template-columns: 1fr 1fr; 
 justify-items: center; 
 align-items: center; 
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
  z-index: 100; 
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

.subtext {
  margin-top: 8px;
}

@media screen and (max-width: 600px) {
  .circulo {
    width: 80%;
    max-width: 250px;
    margin: 20px auto; 
    position: relative; 
    overflow: hidden; 
    border-radius: 50%; /* Formato circular */
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
  padding-left: 0px;
  padding-right: 60px;
  width: 500;
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
