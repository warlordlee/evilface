<template>
  <div id="app">
    <face></face>
  </div>
</template>

<script>
import face from "@/components/face";

export default {
  name: 'App',
  components: {
    face
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
