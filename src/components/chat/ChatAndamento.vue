<template>
  <div class="chat-andamento">
    <q-page padding>
      <p v-for="n in 15" :key="n">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugit nihil
        praesentium molestias a adipisci, dolore vitae odit, quidem consequatur
        optio voluptates asperiores pariatur eos numquam rerum delectus commodi
        perferendis voluptate?
      </p>
    </q-page>
    <div class="chat-area-footer">
      <input type="text" placeholder="Digite uma mensagem" />
      <div class="icon-container">
        <div class="icon-container-esquerdo">
          <q-icon name="emoji_emotions" />
          <q-icon name="attach_file" />
          <q-icon name="videocam" />
        </div>

        <div class="icon-container-direito">
          <q-icon name="mic" />
          <q-icon name="send" />
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
defineOptions({
  name: "ChatAndamento",
});
</script>
<style lang="scss">
.chat-andamento {
  background-image: url("assets/back-conversa.png");
  background-size: contain;
}
.input-field {
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  margin: 0;
  z-index: 100;
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
