<template>
  <main class="message-panel">
    <MessageHeader />
    <div class="message-body">Mian messages</div>
    <MessageFooter />
  </main>
</template>

<script>
import MessageHeader from "@/components/MessageHeader";
import MessageFooter from "@/components/MessageFooter";
export default {
  components: {
    MessageHeader,
    MessageFooter,
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
    flex-grow: 1;
  }
}
</style>
