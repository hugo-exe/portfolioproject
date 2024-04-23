<template>
  <div>

    <v-app-bar app color="black" dark flat class="px-4 px-md-12">
      <v-btn>
        <v-icon color="purple" left class="mr-2">fas fa-code</v-icon>Hugo
      </v-btn>

      <v-btn icon @click="drawer = !drawer" class="d-lg-none"> 
        <v-icon class="fas fa-bars"></v-icon>
      </v-btn>

      <v-toolbar-items class="hidden-sm-and-down"> 
        <v-btn text @click="('inicio')" href="/" class="text-white">Início</v-btn>
        <v-btn text @click="('sobre')" href="/about">Sobre mim</v-btn>
        <v-btn text @click="('projetos')" href="/projetos">Projetos</v-btn>
      </v-toolbar-items>
    </v-app-bar>

    <v-navigation-drawer app v-model="drawer" temporary right>
      <v-list>
        <v-list-item @click="('inicio')" href="/">
          <v-list-item-title>Início</v-list-item-title>
        </v-list-item>
        <v-list-item @click="('sobre')" href="/about"> 
          <v-list-item-title>Sobre mim</v-list-item-title>
        </v-list-item>
        <v-list-item @click="('projetos')" href="/projetos">
          <v-list-item-title>Projetos</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
    };
  },
  methods: {
    scroll(refName) {
      const element = document.getElementById(refName);
      element.scrollIntoView({ behavior: "smooth" });
    },
  },
};
</script>

<style>
.hidden-sm-and-down {
  display: none;
}


@media (min-width: 600px) { 
  .hidden-sm-and-down {
    display: flex;
    align-items: center;
  }
  
  .d-lg-none {
    display: none; 
  }
}
</style>
