<template>
  <h1>Meu banco 2.0 {{text}}</h1>
</template>

<script>
export default {
  name: "Titulo",
  props: {
    text: String,
  },
};
</script>

<style scoped>
h1 {
  color: peru;
}
</style>