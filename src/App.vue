<template>
  <div id="app">
    <div v-for="item in recepies" :key="item.title">
      <RecepieItem :item="item"/> 
    </div>
  </div>
</template>

<script>
import RecepieItem from "./components/RecepieItem.vue";

export default {
  name: "App",
  components: {
    RecepieItem,
  },
  data() {
    return {
      recepies: [],
    };
  },

  mounted() {
    const apiUrl =
      "https://cors-anywhere.herokuapp.com/http://www.recipepuppy.com/api/";
    this.$http.get(apiUrl).then((response) => {
      const recepies = response.data.results;
      console.log(recepies);
      this.recepies = recepies;
    });
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
