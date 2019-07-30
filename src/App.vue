<template>
  <div id="app">
    <Header></Header>
    Postlist
  </div>
</template>

<script>
import Header from "./components/Header"
import Postlist from "./components/Postlist"

export default {
  name: "App",
  components: {
    Header,
    Postlist
  }
};
</script>

<style>
</style>
