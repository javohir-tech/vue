<template>
  <div class="container ">
    <div class="content">
      <AppInfo />
      <SearchPanel />
      <AppFilter/>
      <MovieList />
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
import AppFilter from "./Components/AppFilter/AppFilter.vue";

export default {
  components: {
    AppInfo,
    SearchPanel,
    MovieList,
    MovieAddForm,
    AppFilter
  },
};
</script>
<style>
</style>
