<template>
    <div class="">
        <h3 class="mb-3">Yangi Kino Qo'shish</h3>
        <form @submit.prevent="AddMovie">
            <div class="d-flex gap-3">
                <input v-model="name" type="text" class="form-control" placeholder="Kino Nomi">
                <input v-model.number="viewers" type="number" class="form-control" placeholder="Nechi Marta Ko'rilgan ? ">
            </div>
            <button class="mt-3 btn btn-success w-100" type="submit">Qo'shish</button>
        </form>
    </div>
</template>
<script>
export default {
    data(){
        return {
            name:"",
            viewers:""
        }
    },
    methods: {
            AddMovie(){
                if(!this.name || !this.viewers){
                    alert("Iltimos Barcha maydonlarni to'ldiring");
                    return
                }

                const newMovie = {
                    name: this.name,
                    viewers: this.viewers,
                    favorite: false,
                    like:false
                }

                this.$emit("new-movie", newMovie)

                this.name = "",
                this.viewers = ""
            }
        },
}
</script>
<style></style>