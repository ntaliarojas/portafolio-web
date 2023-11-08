<template>
  <v-app-bar class="transparent-nav" style="background-color: transparent;
                  backdrop-filter: blur(10px);
                  position: fixed;

              ">
    <v-app-bar-title style="color: white;" class="icon">
      <v-icon>
        <img src="@/assets/butterfly.png" alt="Mariposa" style="width: 24px; height: 24px;" />
      </v-icon>
    </v-app-bar-title>
    <v-list class="nave d-flex align-center" style="background-color: transparent;
            color: white;
            ">
      <v-list-item>
        <v-list-item-title class="list">
          <v-btn  href="#inicio">Inicio</v-btn>
          <v-btn href="#about">Sobre mi</v-btn>
          <v-btn href="#Formacion">Formación</v-btn>
          <v-btn href="#portafolio">Portafolio</v-btn>
          <v-btn href="#contacto">Contacto</v-btn>
        </v-list-item-title>
      </v-list-item>
    </v-list>

    <v-menu v-if="showMenu" class="menu">
      <template v-slot:activator="{ props }">
        <v-btn color="white" icon="mdi-dots-vertical" v-bind="props"></v-btn>
      </template>

      <v-list>
        <v-list-item class="lis-menu">
          <v-list-item-title>
            <a style="background-color: transparent;" href="#inicio">Inicio</a>
          </v-list-item-title>
          <v-list-item-title>
            <a href="#about">About</a>
          </v-list-item-title>
          <v-list-item-title>
            <a href="#formacion">Fromación</a>
          </v-list-item-title>
          <v-list-item-title>
            <a href="#portafolio">portafolio</a>
          </v-list-item-title>
          <v-list-item-title>
            <a href="#contacto">Contacto</a>
          </v-list-item-title>

        </v-list-item>
      </v-list>
    </v-menu>
  </v-app-bar>
</template>
  
<script>
export default {
  name: 'headerapp',
  data() {
    return {
      showMenu: false
    };
  },
  mounted() {
    this.showMenu = window.innerWidth <= 850; // Verifica el ancho de la pantalla al cargar la página
    window.addEventListener('resize', this.handleResize);
  },
  beforeUnmount() {
    window.removeEventListener('resize', this.handleResize);
  },
  methods: {
    handleResize() {
      this.showMenu = window.innerWidth <= 800; // Actualiza la visibilidad del menú en función del ancho de la pantalla
    }
  }
};
</script>



<style scoped>
.list:hover {
  color: rgb(204, 215, 106);
}
.lis-menu{
  text-align: center;
}
.lis-menu a{
  text-decoration: none;
  color: black;
}
.lis-menu a:hover{
  color: #d9506d;
}
@media screen and (max-width: 800px) {
  .list {
    visibility: hidden;
    height: 0;
  }
  .icon{
    visibility: hidden;
    height: 0;
  }
}

@media screen and (max-width: 300px) {
  .menu {
    right: -30rem;
  }
}
</style>