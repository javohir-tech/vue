<template>
    <li class="movie-list__item mb-3 align-items-center list-group-item  d-flex justify-content-between"
        :class="{ 'text-warning': kino.favorite }" style="background-color: transparent;">
        <div>
            <h3 class="fs-4">{{ kino.name }}</h3>
        </div>
        <div class="d-flex align-items-center gap-5">
            <h3 class="mb-0 fs-4 text-center">{{ kino.viewers }}</h3>
            <div class="d-flex gap-3 movie-list__icons">
                <button @click="$emit('toggle-favorite', kino)" type="button" class="btn btn-sm "><i
                        class="bi bi-film text-warning py-2 px-3 rounded"></i></button>
                <button @click="$emit('toggle-delete', kino)" type="button" class="btn btn-sm"><i
                        class="bi bi-trash-fill text-danger py-2 px-3 rounded"></i></button>
                <button @click="$emit('toggle-like', kino)" type="button" class="btn btn-sm"><i
                        class="bi  text-warning py-2 px-3 rounded"
                        :class="[kino.like ? 'bi-star-fill' : 'bi-star']"></i></button>
            </div>
        </div>
    </li>
</template>
<script>
// import { ref } from "vue"

export default {
    props: {
        kino: {
            type: Object,
            required: true
        }
    },
    setup() {

    }
}
</script>
<style scoped>
.movie-list__icons .btn {
    background-color: #F1F0E9;
}
</style>