<template>
 <v-app id="projetos">
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
   <v-col cols="12" class="imgHover">
    <v-row class="fill-height" align="center" justify="center">
      <template v-for="(item, i) in items" :key="i">
        <v-col cols="12" md="4" v-for="(item, i) in items" :key="i" class="mt-4 mb-4">
        <v-hover v-slot="{isHovering, props}">
        <v-card :elevation="isHovering ? 12: 2" :class="{'on-hover' : isHovering}" v-bind="props" class="black-card">
        <v-img :src="item.img" height="225px" cover></v-img>
        </v-card>
        </v-hover>
      </v-col>
      </template>
    </v-row>
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
  name: "ProjectsView",
  components: {
    NavBar,
  },
  data() {
    return {
      items: [
        { id: 1, src: require('@/assets/img/X.png') },
        { id: 2, src: require('@/assets/img/X.png') },
        { id: 3, src: require('@/assets/img/X.png') },
      ],
    };
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

.arrow-down {
  position: absolute;
  z-index: 9999;
  bottom: 15px;
  left: 50%;
  transform: translateX(-50%);
  text-align: center;
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


.mt-16 {
 padding-bottom: 16px;
}
.first {
 width: 100%;
 height: 280px;
 text-align: center;
 padding: 2rem 2rem;
}
.child {
 display: inline-block;
 padding: 2rem 1rem;
 text-align: center;
}
.imgHover {
 padding: 0 200px;
}
.black-card {
  text-align: center;
  background-color: rgb(83, 81, 83);
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


@media (max-width: 960px) {
  .head {
    height: auto;
  }
  .arrow-down {
    bottom: 5px;
  }
  .imgHover {
    padding: 0 8px;
  }
}

@media (max-width: 600px) {

  .mt-16{
    padding-bottom: 16px;
  }
  .head {
    padding: 6px;
  }
  .arrow-down {
    bottom: 2px;
  }
  .imgHover {
    padding: 0 4px;
  }
  .head h1 {
    font-size: 1.5em; 
  }
  .arrow-down v-icon {
    font-size: 1.5em; 
  }
  #footer-contatos {
  height: 60px;
}
}

</style>
