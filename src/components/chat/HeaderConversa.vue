<template>
  <div id="header-conversa">
    <q-header elevated>
      <q-toolbar class="bar-conversa" unelevated>
        <div class="bar-conversa__perfil">
          <q-avatar size="48px">
            <img src="~assets/usuarios/1.svg" />
          </q-avatar>
          <div class="bar-conversa__perfil__infor">
            <div class="bar-conversa__perfil__infor--titulo">João Gomes</div>
            <div class="bar-conversa__perfil__infor--valor">
              <q-icon name="sentiment_satisfied_alt" />
              <span class="classificacao">2,5</span>
            </div>
          </div>
        </div>

        <q-space />

        <div class="bar-conversa__opcoes">
          <q-btn unelevated dense color="purple-4" icon="card_giftcard" />
          <q-btn unelevated dense color="orange-4" icon="local_phone" />
          <q-btn unelevated dense color="teal-4" icon="refresh" />
          <q-btn unelevated dense color="blue-5" icon="sync_alt" />
          <q-btn unelevated dense color="red-3" icon="phone_disabled" />
        </div>

        <q-btn
          flat
          @click="fecharConversas"
          round
          dense
          icon="more_vert"
          class="bar-conversa-mais"
        />
      </q-toolbar>
    </q-header>
  </div>
</template>

<script setup>
const emit = defineEmits(["fecharConversas"]);

defineOptions({
  name: "HeaderConversa",
});

const fecharConversas = () => {
  emit("fecharConversas");
};
</script>
<style lang="scss">
#header-conversa {
  .bar-conversa {
    background: #ffffff;
    height: 64px;

    .bar-conversa__perfil {
      display: flex;
      color: red;
      gap: 15px;
      align-items: center;
      .bar-conversa__perfil__infor {
        display: flex;
        flex-direction: column;
        gap: 0px;

        .bar-conversa__perfil__infor--titulo {
          font-size: 20px;
          color: #262626;
          font-weight: 500;
          margin-bottom: -5px;
        }

        .bar-conversa__perfil__infor--valor {
          display: flex;
          font-size: 12px;
          color: #eb5757;
          align-items: center;
          gap: 5px;

          .classificacao {
            font-weight: 700;
          }
        }
      }
    }

    .bar-conversa__opcoes {
      display: flex;
      gap: 9px;
      align-items: center;
      margin-right: 20px;
    }
  }
  .bar-conversa-mais {
    color: #9e9e9e;
  }
}
</style>
