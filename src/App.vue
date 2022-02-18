<template>
  <div id="App">
    <div class="character" v-for="personaje in personajes" :key="personaje">
      <div class="container">
        <img class="image" :src="personaje.src" alt="">
      <p class="texto">{{personaje.nombre}}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      
      personajes: [
        {
          nombre: "Rick Sanchez",
          src: "https://rickandmortyapi.com/api/character/avatar/1.jpeg",
        },
        {
          nombre: "Morty Smith",
          src: "https://rickandmortyapi.com/api/character/avatar/2.jpeg",
        },
        {
          nombre: "Summer Smith",
          src: "https://rickandmortyapi.com/api/character/avatar/3.jpeg",
        },
        {
          nombre: "Beth Smith",
          src: "https://rickandmortyapi.com/api/character/avatar/4.jpeg",
        },
        {
          nombre: "Jerry Smith",
          src: "https://rickandmortyapi.com/api/character/avatar/5.jpeg",
        },
      ],
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

body {
   background: url("https://rickandmortypod.com/wp-content/uploads/2018/11/cropped-RM_page-header_background1-3.png");
}

  .image{
    border-radius: 50%;
    width: 6%;
  }

  .container{
    display: flex;
    align-items: center;
    padding: 3% 0% 0% 5%;
  }

  .texto{
    margin-left: 2%;
    color: green;
    font-size: xx-large;
  }

</style>