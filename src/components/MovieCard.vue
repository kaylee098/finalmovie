<!-- Kaylee Martin -->
<!-- CardComponent Template Page -->
<!-- the template that will be used to create the movie cards -->
<template>
    <div class="card" >
        <img :src=imgPath class="card-img-top" alt="..." style="height:24rem; border:3px solid black;">
        <div class="card-body">
            <!-- information brought in by app.vue vue instance -->
            <!-- movie title -->
            <h5 class="card-title">{{movie.title}}</h5>
            <!-- overall overview of the movie -->
            <p class="card-text">{{movie.overview}}</p>
            <!-- price of movie ticket -->
            <p class="card-text">Price: $12.55</p>
        </div>
           <!-- buy ticket button that should add the movie title and price to the shopping cart once clicked -->
         <a href="#" data-name="movie.title" data-price="12.55" class="add-to-cart btn btn-primary">Buy Ticket</a>
    </div>
</template>

<script>
    export default({
        name: 'MovieCard',
        props:['movie'],
        data(){
            return {
                // pulls the correct image from the array poster path
                imgPath:  "https://image.tmdb.org/t/p/w500/" + this.movie.poster_path
            }
        }
        
    })

</script>


<style>
.card{
    width:28.5rem;
    color:black;
    background-color:lightgoldenrodyellow;
}


</style>