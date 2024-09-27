<template>
  <div id="faixa-atendimento">
    <div class="tab-atendimento">
      <q-tabs
        :model-value="tab"
        @update:model-value="(newTab) => $emit('update:tab', newTab)"
        style="border-bottom: 2px solid #dadada"
        class="tab-atendimento-top"
      >
        <q-tab name="ativos" label="Ativos" />
        <q-tab name="pendentes" label="Pendentes" />
        <q-tab name="grupos" label="Grupos" />
        <q-tab name="fechados" label="Fechados" />
      </q-tabs>
    </div>
  </div>
</template>

<script setup>
import { defineProps, defineEmits } from "vue";

defineOptions({
  name: "TabAtendimento",
});

const props = defineProps({
  tab: {
    type: String,
    required: true,
  },
});

const emit = defineEmits(["update:tab"]);
</script>
<style lang="scss">
#tab-atendimento {
  .tab-atendimento {
  }
}

.tab-atendimento-top {
  border-radius: 11px;
  color: #a8a8a8 !important;
  border: 1px solid #dadada;

  .q-tab__label {
    text-transform: none !important;
  }
  .q-tab--active {
    background: #0098fd;
    color: #ffffff;
  }
  .q-tab__indicator.absolute-bottom {
    color: #0098fd;
  }
}
</style>
