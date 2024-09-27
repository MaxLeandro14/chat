<template>
  <div id="faixa-atendimento">
    <div class="faixa-atendimento">
      <div class="view-container faixa-atendimento__container">
        <div class="faixa-atendimento__titulo">Atendimento</div>
        <div class="faixa-atendimento__voltar">
          <q-btn round unelevated dense color="white" size="11px">
            <q-icon name="arrow_back" color="blue-7" size="16px" />
          </q-btn>

          <span> Menu </span>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
defineOptions({
  name: "FaixaAtendimento",
});
</script>
<style lang="scss">
#faixa-atendimento {
  .faixa-atendimento {
    background-color: #0098fd;
    height: 48px;

    .faixa-atendimento__container {
      display: flex;
      justify-content: space-between;
      align-items: center;
      height: 100%;
      color: #ffffff;
      font-size: 18px;
      font-weight: 700;

      .faixa-atendimento__voltar {
        display: flex;
        gap: 10px;
      }
    }
  }
}
</style>
