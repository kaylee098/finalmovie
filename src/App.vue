<!-- Kaylee Martin -->
<!-- Due: 12/12/2022 -->
<!-- TMDB Final Project using Vue, Axios, Bootstrap -->

<!-- template for overall page, main page -->
<template>
  <div id="app">
    <!-- navbar implementation -- on navbar.vue -->
    <NavBar></NavBar>
    <!-- card component setup -->
    <div class="row row-cols-1 row-cols-md-2 g-4">
        <MovieCard class="col"  v-for="show in tvshows" v-bind:key="show.id" :movie="show"></MovieCard>
    </div>
    <ShoppingCart></ShoppingCart>
    <MovieFooter></MovieFooter>
  </div>
</template>

<script>
import 'bootstrap'
import 'bootstrap/dist/css/bootstrap.min.css'
import MovieCard from './components/MovieCard.vue';
import NavBar from './components/NavBar.vue'
import ShoppingCart from './components/ShoppingCart.vue'
import MovieFooter from './components/MovieFooter.vue'
import axios from 'axios'

// includes app, pulling together the cardcomponent and navbar
export default {
  name: 'App',
  components: {
    NavBar,
    MovieCard,
    ShoppingCart,
    MovieFooter
  },
  // retrieving movie data
  data(){
    return{
      tvshows:[],
    }
  },
  mounted(){
    axios
    // API Call for now playing movies
    // My API Key  61e97aeda24257e41c374d7596d49757
    .get("https://api.themoviedb.org/3/movie/now_playing?api_key=61e97aeda24257e41c374d7596d49757&language=en-US&page=1")
    // array response
    .then((response) => {
      // determines how many movie cards there are, currently there are three
      this.tvshows = response.data.results.slice(0,3);
      // print to the console the array information being grabbed
      console.log(this.tvshows)
    })
  }
}
</script>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-size:15px;
  color: #2c3e50;
  margin-top: 0px;
  padding-left:0px;
  background-color:slategray;
  font-family:'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif
}
</style>