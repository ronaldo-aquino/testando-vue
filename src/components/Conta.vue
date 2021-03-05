<template>
  <h2>Tipo de conta: {{ conta }}</h2>
  <h2>Saldo: {{ saldo }}</h2>
  <h2>Conta: {{ estado ? "Ativa" : "Desativada" }}</h2>
  <div v-for="(servico, index) in servicos" :key="index">
    {{ index + 1 }} - {{ servico }}
  </div>
  <AcaoSaldo text="Aumentar" @acao="aumentar" />
  <AcaoSaldo text="Diminuir" @acao="diminuir" :desativar="desativar" />
</template>

<script>
import AcaoSaldo from "./AcaoSaldo";

export default {
  name: "Conta",
  components: {
    AcaoSaldo,
  },
  data() {
    return {
      conta: "Corrente",
      saldo: 1000,
      estado: true,
      servicos: ["Trnaferência", "Pagamentos", "Financiamentos"],
      desativar: false,
    };
  },

  methods: {
    aumentar() {
      this.desativar = false;
      this.saldo = this.saldo + 100;
    },
    diminuir() {
      if (this.saldo === 0) {
        alert("Sem saldo");
        this.desativar = true;
        return;
      }
      this.saldo = this.saldo - 100;
    },
  },
};
</script>

<style scoped>
</style>