<template>
  <button @click="acao" :disabled="desativar">{{ text }}</button>
</template>

<script>
export default {
  name: "AcaoSaldo",
  props: {
    text: String,
    desativar: {
      type: Boolean,
      defaukt: false,
    },
  },
  methods: {
    acao() {
      this.$emit("acao");
    },
  },
};
</script>

<style scoped>
</style>