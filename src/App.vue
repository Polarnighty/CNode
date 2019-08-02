<template>
  <div id="app">
    <Header></Header>
    <div class="main">
      <router-view name="slidebar"></router-view>
      <router-view name="main"></router-view>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header";
import Postlist from "./components/Postlist";

export default {
  name: "App",
  components: {
    Header,
    Postlist
  }
};
</script>

<style>
#app {
  background-color: #e1e1e1;
  min-height: 100vh;
}
* {
  margin: 0;
  padding: 0;
}
.main {
  width: 90%;
  margin: 0 auto;
}
</style>
