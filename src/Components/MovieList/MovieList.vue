<template>
    <div class="shadow-lg mb-5">
        <ul class="movie-list">
            <MovieListItem v-for="(film, index) in kinolar" :kino="film" :key="index" @toggle-like="toggleLike" @toggle-favorite="toggleFavorite" @toggle-delete="toggleDelete" />
        </ul>
       <div class="px-3 px-2 mt-5">
        <MovieAddForm @new-movie="addNewMovie"/>
       </div>
    </div>
</template>

<script>
import MovieListItem from '../Movie-list-item/MovieListItem.vue';
import MovieAddForm from '../MovieAddForm/MovieAddForm.vue';

export default {
    components: {
        MovieListItem,
        MovieAddForm
    },
    data() {
        return {
            kinolar: [
                {
                    name: "Taxtlar o'yini",
                    viewers: 1021,
                    like: true,
                    favorite: false
                },
                {
                    name: "Titanlar Hujumi",
                    viewers: 121,
                    like: false,
                    favorite: true
                },
                {
                    name: "Interterstelar",
                    viewers: 21,
                    like: false,
                    favorite: true
                },
            ]
        }
    },
    methods: {
        toggleLike(kino) {
            kino.like = !kino.like
        },
        toggleFavorite(film){
            film.favorite = !film.favorite
        },
        toggleDelete(kino){
            this.kinolar = this.kinolar.filter(film =>film  !== kino)
        },
        addNewMovie(newMovie){
            this.kinolar.push(newMovie)
        }
    }
}
</script>
<style></style>