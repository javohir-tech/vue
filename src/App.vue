<template>
  <div class="container ">
    <div class="content">
      <AppInfo />
      <SearchPanel />
      <MovieList :kinolar="kinolar"/>
      <MovieAddForm />
    </div>
  </div>
</template>

<script>
//styles
import "./App.css";
//components
import AppInfo from "./Components/AppInfo/AppInfo.vue";
import MovieAddForm from "./Components/MovieAddForm/MovieAddForm.vue";
import MovieList from "./Components/MovieList/MovieList.vue";
import SearchPanel from "./Components/SearchPanel/SearchPanel.vue";

export default {
  components: {
    AppInfo,
    SearchPanel,
    MovieList,
    MovieAddForm,
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
};
</script>
<style></style>
