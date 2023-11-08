<template>
  <v-row class="header" id="inicio">
    <v-col lg="12" md="12" class="mt-6 text-center">
      <div>
        <v-img class="foto-me" src="../assets/me2.jpg" cover alt="Imagen"></v-img>
      </div>
      <div>
        <p class="paragraph-me">Hola, Soy Natalia <span class="sp-last">Rojas</span></p>
        <p>Desarrolladora web Front-End</p>
        <p>@lamonroee</p>
      </div>
    </v-col>

    <v-col lg="12" md="12">
      <h2 class="text-info ">Construyendo puentes <br> entre creatividad <br> & tecnología.</h2>
      <p class="description">Tecnologa en analisis y desarrollo de sistemas de infrormacion <br> y estudiante
        en
        diseño de Aplicaciones moviles <br> con +8 meses de experiencia como <br> desrrolladora web</p>
    </v-col>
    <v-col lg="12" md="12" class="gamer mt-6 ">
      <div>
        <v-img class="img-ab" src="../assets/a-removebg-preview.png" cover alt="Imagen"></v-img>
      </div>
    </v-col>
  </v-row>
</template>

<script>

export default {
  name: 'HelloWorld'
}
</script>


<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400&display=swap');



* {
  color: white;
  margin-left: 0;

}

.gamer {
  padding-top: 2rem;
}

.img-ab {
  width: 20rem;
  margin: 0 auto;
  margin-bottom: -1.1rem;
}


.header {

  position: relative;
  min-height: 35rem;
  background-repeat: repeat;
  text-align: center;
  background-color: #2a2f3d;

}

.header::after {
  bottom: 74%;
  content: "";
  position: absolute;
  left: 2%;
  width: 150px;
  height: 350px;
  background-image: url(../assets/puntos.png);
  background-size: contain;
}



.head2 {
  margin-top: 6%;
}

.foto-me {
  margin: 0 auto;
  width: 20rem;
  border-radius: 50%;
}

.text-info {
  color: white !important;
  font-family: 'Poppins', sans-serif;
  max-width: 100%;
  font-size: 3rem;
  line-height: 1;
  font-weight: bold;
  text-align: center;
  margin: calc(4rem - 1rem) auto 0 auto;

}

.description {
  color: #d76a82;
  font-size: 1rem;
  text-align: center;
  margin: 0 auto;
  padding-top: 2rem;
  line-height: 1.2;
}

.paragraph-me {
  font-family: 'Poppins', sans-serif;
  font-size: 2rem;
  color: white;
}

.sp-last {
  font-size: 3rem;
  font-weight: bold;
  font-family: 'Croissant One', cursive;
}

@media screen and (max-width: 414px) {
  .foto-me {
    margin: 0 auto;
    width: 15rem;
    border-radius: 50%;
  }

  .text-info {

    font-size: 1.5rem;
    margin: calc(4rem - 1rem) auto 0 auto;

  }

  .description {
    font-size: 0.80rem;
    margin: calc(3rem - 2rem) auto 0 auto;

  }


}

@media screen and (max-width: 538px) {

  .header::after {
    bottom: 77%;
    content: "";
    position: absolute;
    left: -2%;
    width: 150px;
    height: 300px;
    background-image: url(../assets/puntos.png);
    background-size: contain;
  }

  .text-info {
    font-size: 2.3rem;
    margin: calc(2rem - 1rem) auto 0 auto;
  }

  .sp-last {
    font-size: 2rem;
    font-weight: bold;
    font-family: 'Croissant One', cursive;
  }
}

@media screen and (max-width: 856px) {
  .header {}

  .header::after {
    bottom: 66%;
    content: "";
    position: absolute;
    left: 2%;
    width: 150px;
    height: 300px;
    background-image: url(../assets/puntos.png);
    background-size: contain;
  }

  .description {
    margin: calc(3rem - 2rem) auto 0 auto;


  }
}

@media screen and (max-width: 391px) {
  .gamer {
    padding-top: 4rem;
  }

  .description {
    color: #d76a82;
    font-size: 1rem;
    text-align: center;
    margin: 0 auto;
    line-height: 1.2;
  }


  .header::before {
    display: none;
  }

  .text-info {
    font-size: 1.5rem;
    margin: calc(1rem - 0rem) auto 0 auto;
  }

  .header::after {
    bottom: 69%;
    content: "";
    position: absolute;
    left: 2%;
    width: 39px;
    height: 300px;
    background-image: url(../assets/puntos.png);
    background-size: contain;
  }

  .sp-last {
    font-size: 2rem;
    font-weight: bold;
    font-family: 'Croissant One', cursive;
  }

  .paragraph-me {
    font-family: 'Poppins', sans-serif;
    font-size: 1.5rem;
    color: white;
  }
}</style>
