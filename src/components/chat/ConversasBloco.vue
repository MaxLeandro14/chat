<template>
  <div id="conversas-bloco">
    <q-layout view="lHh Lpr lff" container style="height: calc(100vh - 118px)">
      <header-conversa @fecharConversas="handleFecharConversas" />

      <q-drawer
        v-model="drawer"
        show-if-above
        :width="400"
        :breakpoint="400"
        class="container-contatos"
      >
        <tab-atendimento v-model:tab="tab" />

        <q-scroll-area style="height: calc(100% - 61px); margin-top: 10px">
          <q-list padding>
            <q-item clickable v-ripple>
              <bloco-contato />
            </q-item>
          </q-list>
        </q-scroll-area>
      </q-drawer>

      <q-page-container>
        <chat-andamento />
      </q-page-container>
    </q-layout>
  </div>
</template>
<script setup>
import HeaderConversa from "components/chat/HeaderConversa.vue";
import TabAtendimento from "components/chat/TabAtendimento.vue";
import ChatAndamento from "components/chat/ChatAndamento.vue";
import BlocoContato from "components/chat/BlocoContato.vue";

import { ref } from "vue";

defineOptions({
  name: "ConversasBloco",
});

const drawer = ref(false);

const tab = ref("ativos");

const text = ref("Field content");

const handleFecharConversas = () => {
  console.log("Evento fecharConversas capturado!");
  drawer.value = !drawer.value;
};
</script>
<style lang="scss">
#conversas-bloco {
  .container-contatos {
    padding: 16px;
  }
  .q-item {
    border-left: 4px solid #e2b93b;
    border-bottom: 1px solid #f1f1f1;
  }
}

.input-field {
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  margin: 0;
  z-index: 100;
}
.container-contatos {
}
.chat-area-footer {
  display: flex;
  width: 100%;
  align-items: center;
  background-color: #eaf3fa;
  position: sticky;
  bottom: 0;
  left: 0;
  padding: 6px 11px;
  flex-direction: column;
}
input {
  border: 2px solid white;
  color: rgb(94, 93, 93);
  background-color: #ffffff;
  padding: 12px;
  border-radius: 6px;
  font-size: 15px;
  margin: 0 12px;
  width: 100%;
  padding-bottom: 36px;
  position: relative;

  &::placeholder {
    color: #8c8c8c;
  }
  &:focus {
    border: 2px solid #0098fd;
    outline: none;
  }
}
.icon-container {
  display: flex;
  justify-content: space-between;
  position: absolute;
  bottom: 13px;
  width: 100%;
  padding: 0px 25px;
  color: #999999;
  font-size: 18px;
}
.icon-container-esquerdo,
.icon-container-direito {
  display: flex;
  align-items: center;
  gap: 11px;

  > * {
    cursor: pointer;
  }
  > *:hover {
    transform: scale(1.1);
    color: #0098fd;
  }
}
</style>
