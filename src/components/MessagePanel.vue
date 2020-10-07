<template>
  <main class="message-panel">
    <MessageHeader />
    <div class="message-body">
      <Message
        :isMessageIn="true"
        message="Me podrian ayudar he estado presentando algunos problemas."
      />
      <Message
        :isMessageIn="false"
        message="¿Me podría proporcionar su número de cuenta?"
      />
      <div class="message-date">21 de Septiembre, 2020</div>
      <div class="message-status">
        La conversación cambió de “No Asignada ” a “Asignada”
      </div>
      <Message :isMessageIn="true" message="Claro mi cuenta es 99613621" />
      <Message
        :isMessageIn="false"
        message="Gracias, voy a verificar en el sistema y revisar el problema."
      />
      <Message
        :isMessageIn="true"
        message="Lorem ipsum dolor sit amet, consectetur adipiscing elit."
      />
      <div class="message-date">Hoy</div>
      <Message :isMessageIn="false" message="Lorem ipsum dolor sit amet" />
      <Message :isMessageIn="false" message="Lorem ipsum " />
      <Message
        :isMessageIn="true"
        message="Nam id nibh lorem. Vestibulum ante ipsum primis in faucibus"
      />
    </div>
    <MessageFooter />
  </main>
</template>

<script>
import MessageHeader from "@/components/MessageHeader";
import MessageFooter from "@/components/MessageFooter";
import Message from "@/components/Message";
export default {
  name: "MessagePanel",
  components: {
    MessageHeader,
    MessageFooter,
    Message,
  },
};
</script>

<style lang="scss" scoped>
.message-panel {
  display: flex;
  flex-direction: column;
  height: calc(100vh - 60px);
  grid-area: main;

  .message-body {
    padding: 24px 32px;
    flex-grow: 1;
    overflow: scroll;

    .message-date,
    .message-status {
      font-size: 14px;
      text-align: center;
      color: $secondary-text;
      margin-bottom: 24px;
    }
  }
}
</style>
