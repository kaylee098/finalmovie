<template>
    <div class="card" style="width: 18rem;">
        <img :src=imgPath class="card-img-top" alt="...">
        <div class="card-body">
            <h5 class="card-title">{{movie.name}}</h5>
            <p class="card-text">{{movie.overview}}</p>
            <a href="#" class="btn btn-primary">Go somewhere</a>
        </div>
    </div>
</template>

<script>
    export default({
        name: 'CardComponent',
        props:['movie'],
        data(){
            return {
                imgPath:  "https://image.tmdb.org/t/p/w500/" + this.movie.poster_path
            }
        }
        
    })

</script>
