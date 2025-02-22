<template>
    <div class="shadow-lg mb-5">
        <ul class="movie-list">
            <MovieListItem/>
            <MovieListItem/>
            <MovieListItem/>
        </ul>
    </div>
</template>

<script>
import MovieListItem from '../Movie-list-item/MovieListItem.vue';

export default {
    components:{
        MovieListItem
    }
}
</script>
<style>
    
</style>