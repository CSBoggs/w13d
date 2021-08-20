<template>
  <div>
    <Page-Body/>
  </div>
</template>

<script>
import PageBody from './components/Page-Body.vue';

export default {
  name: "App",
  components: {
    PageBody
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
