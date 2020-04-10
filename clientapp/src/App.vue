<template>
  <div id="app">
    <Retro />
  </div>
</template>

<script>
import Retro from './components/Retrospective.vue';

export default {
  name: 'App',
  components: {Retro}
}
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
