<template>
  <div class="bloco-contato">
    <div class="bloco-contato__avatar">
      <q-avatar size="60px">
        <img src="~assets/usuarios/1.svg" />
      </q-avatar>
    </div>
    <div class="bloco-contato__infor">
      <div class="bloco-contato__infor__esquerda">
        <div class="bloco-contato__infor__avatar">
          <q-icon name="fa-brands fa-whatsapp" color="green" />
          <span class="bloco-contato__infor__nome">André Gomes</span>
        </div>
        <div class="bloco-contato__infor__esquerda__dinamico">
          <div class="bloco-contato__infor__esquerda__dinamico__escrevenedo">
            <span class="escrevendo">
              Escrevendo <span class="pontos">...</span>
            </span>
          </div>
        </div>
        <div class="bloco-contato__infor__tags">
          <q-badge color="blue-4"> White label </q-badge>
          <q-badge color="orange-4"> Suporte </q-badge>
          <q-badge color="red-3"> Lead quente </q-badge>
        </div>
      </div>

      <div class="bloco-contato__infor__direita">
        <div class="bloco-contato__infor__direita__data">11/16/19</div>
        <div class="bloco-contato__infor__direita__contagem-conversa">
          <q-badge rounded color="blue" label="1" />
        </div>
        <div class="bloco-contato__infor__direita__id">#16011986</div>
      </div>
    </div>
  </div>
</template>
<script setup>
defineOptions({
  name: "BlocoContato",
});
</script>
<style lang="scss">
.bloco-contato {
  display: flex;
  gap: 10px;
  align-items: center;
  padding: 5px;
  width: 100%;

  .bloco-contato__infor {
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .bloco-contato__infor__esquerda {
    min-height: 81px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;

    .bloco-contato__infor__avatar {
      display: flex;
      align-items: center;

      .bloco-contato__infor__nome {
        font-size: 16px;
        font-weight: 500;
        color: #262626;
        margin-left: 5px;
      }
    }

    .bloco-contato__infor__esquerda__dinamico {
      margin: 6px 0px;
      .bloco-contato__infor__esquerda__dinamico__escrevenedo {
        display: flex;
        gap: 5px;
        align-items: center;

        .escrevendo {
          color: #2f80ed;
          font-size: 14px;
        }
      }
    }

    .bloco-contato__infor__tags {
      display: flex;
      gap: 3px;
      flex-wrap: wrap;

      .q-badge {
        font-size: 10px;
      }
    }
  }
  .bloco-contato__infor__direita {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    height: 100%;
    min-height: 84px;
    align-items: end;

    .bloco-contato__infor__direita__data {
      font-size: 14px;
      color: #999999;
      font-weight: 400;
      display: flex;
      justify-content: right;
    }
    .bloco-contato__infor__direita__id {
      color: #a8a8a8;
      font-size: 10px;
    }
    .bloco-contato__infor__direita__contagem-conversa {
      font-size: 18px;
      .q-badge {
        font-size: 18px;
      }
    }
  }
}
.pontos {
  display: inline-block;
  width: 1em;
  text-align: left;
  animation: piscar 2.5s steps(4, end) infinite;
}
@keyframes piscar {
  0% {
    visibility: hidden;
  }
  25% {
    visibility: visible;
  }
  50% {
    visibility: hidden;
  }
  75% {
    visibility: visible;
  }
  100% {
    visibility: visible;
  }
}
</style>
