<template>
    <li class="movie-list__item align-items-center list-group-item  d-flex justify-content-between":class="{'text-warning' : isActive}"
        style="background-color: transparent;">
        <div>
            <h3 class="fs-4">Taxtlar O'yini </h3>
        </div>
        <div class="d-flex align-items-center gap-5">
            <h3 class="mb-0 fs-4">1021</h3>
            <div class="d-flex gap-3 movie-list__icons">
                <button @click="toggle" type="button" class="btn btn-sm "><i
                        class="bi bi-film text-warning py-2 px-3 rounded"></i></button>
                <button type="button" class="btn btn-sm"><i
                        class="bi bi-trash-fill text-danger py-2 px-3 rounded"></i></button>
                <button type="button" class="btn btn-sm"><i
                        class="bi bi-star text-warning py-2 px-3 rounded"></i></button>
            </div>
        </div>
    </li>
</template>
<script>
import { ref } from "vue"

export default {
    setup() {
        const isActive = ref(false);

        const toggle = () => {
            isActive.value = !isActive.value
        }

        return { isActive, toggle }
    }
}
</script>
<style scoped>
.movie-list__icons .btn {
    background-color: #F1F0E9;
}
</style>