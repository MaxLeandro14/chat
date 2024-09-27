<template>
  <faixaAtendimento />
  <conversasBloco />
</template>

<script setup>
import FaixaAtendimento from "components/chat/FaixaAtendimento.vue";
import ConversasBloco from "components/chat/ConversasBloco.vue";

defineOptions({
  name: "ChatPage",
});
</script>
