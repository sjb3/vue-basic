<template>
  <div id="app">
    <img src="./assets/bowie.jpg" />
    <!--<audio controls>
      <source type="audio/mpeg" src="./assets/dance.mp3" />
    </audio>-->
    <test></test>
    <users></users>
  </div>
</template>

<script>
import Test from './components/test';
import Users from './components/users';
export default {
  name: 'app',
  components: {
    Test,
    Users
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 2px;
  background-color: #bfafaf;
}
</style>
