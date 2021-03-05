<template>
  <Titulo />
  <Conta />
</template>

<script>
import Titulo from "./components/Titulo";
import Conta from "./components/Conta";

export default {
  name: "App",
  components: {
    Titulo,
    Conta,
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
