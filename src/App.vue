<template>
  <div id="app">
    <Header />
    <ChatList />
    <Message />
  </div>
</template>

<script>
import Header from "@/components/Header";
import ChatList from "@/components/ChatList";
import Message from "@/components/Message";

export default {
  components: {
    ChatList,
    Header,
    Message,
  },
};
</script>

<style lang="scss">
@import "./sass/_basic.scss";
#app {
  display: grid;
  grid-template-columns: 320px 1fr 320px;
  grid-template-rows: max-content;
  grid-template-areas:
    "header   header header"
    "chatlist main   aside";
}
</style>
