<template>
  <div id="menu-horizontal">
    <div class="view-container menu-horizontal-container">
      <div class="menu-horizontal-logo">
        <img alt="logo" src="~assets/Logo.svg" />
      </div>
      <div class="menu-horizontal-itens">
        <div class="menu-horizontal-itens__btn">
          <q-btn
            no-caps
            unelevated
            class="backgrund-primary color-segundary"
            text-color="#0098FD"
          >
            <q-icon left name="filter_alt" />
            <div>Pipeline</div>
          </q-btn>

          <q-btn no-caps unelevated class="backgrund-primary color-segundary">
            <q-icon left name="task" />
            <div>Tarefas</div>
          </q-btn>

          <q-btn no-caps unelevated class="backgrund-primary color-segundary">
            <q-icon left name="group" />
            <div>Gestão de leads</div>
          </q-btn>
        </div>

        <q-separator vertical spaced />

        <div class="menu-horizontal-itens__icons">
          <q-btn no-caps unelevated flat color="grey" icon="chat" />

          <q-btn
            unelevated
            round
            dense
            icon="notifications"
            class="custom-grey-icon"
          >
            <q-badge color="#0098FD" floating>4</q-badge>
          </q-btn>
        </div>

        <q-separator vertical spaced />

        <div class="menu-horizontal-itens__menu">
          <div class="menu-horizontal-itens__menu__dados">
            <span class="menu-horizontal-itens__menu__dados__nome">
              Daniel Silveira
            </span>
            <span class="menu-horizontal-itens__menu__dados__perfil">
              Gerência
            </span>
          </div>
          <q-btn-dropdown round flat class="backgrund-primary">
            <q-list>
              <q-item clickable v-close-popup @click="onItemClick">
                <q-item-section>
                  <q-item-label>Photos</q-item-label>
                </q-item-section>
              </q-item>

              <q-item clickable v-close-popup @click="onItemClick">
                <q-item-section>
                  <q-item-label>Videos</q-item-label>
                </q-item-section>
              </q-item>

              <q-item clickable v-close-popup @click="onItemClick">
                <q-item-section>
                  <q-item-label>Articles</q-item-label>
                </q-item-section>
              </q-item>
            </q-list>
          </q-btn-dropdown>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
defineOptions({
  name: "MenuHorizontal",
});

const props = defineProps({
  title: {
    type: String,
    required: true,
  },

  caption: {
    type: String,
    default: "",
  },

  link: {
    type: String,
    default: "#",
  },

  icon: {
    type: String,
    default: "",
  },
});
</script>
<style lang="scss">
#menu-horizontal {
  .menu-horizontal-container {
    height: 70px;
    background: #ffffff;
    display: flex;
    align-items: center;
    justify-content: space-between;

    .menu-horizontal-itens {
      display: flex;
      gap: 5px;

      > * {
        display: flex;
        gap: 10px;
      }

      .menu-horizontal-itens__btn {
        > * {
          border-radius: 8px;
        }
      }

      .menu-horizontal-itens__menu {
        .menu-horizontal-itens__menu__dados {
          display: flex;
          flex-direction: column;
          margin-left: 20px;

          .menu-horizontal-itens__menu__dados__nome {
            font-size: 14px;
            color: #666666;
            font-weight: 500;
          }

          .menu-horizontal-itens__menu__dados__perfil {
            font-size: 12px;
            color: #0098fd;
            font-weight: 400;
          }
        }
      }

      .menu-horizontal-itens__icons {
        .custom-grey-icon .q-icon {
          color: #9e9e9e;
        }
      }
    }
  }
}
</style>
