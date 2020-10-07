<template>
  <div class="chatlist">
    <div class="chatlist__search">
      <InputSearch />
    </div>
    <ul class="chatlist__container">
      <ChatListItem
        v-for="(customer, index) in customers"
        :key="index"
        :customer="customer"
      />
    </ul>
  </div>
</template>

<script>
import ChatListItem from "@/components/ChatListItem.vue";
import InputSearch from "@/components/InputSearch.vue";
export default {
  name: "ChatList",
  data() {
    return {
      customers: [
        {
          name: "Jane Cooper",
          message: "Ya he realizado las recomendaciones ...",
          avatarImage: "avatar-customer",
          isOnline: true,
          iconPlatform: "whatsapp",
          active: true,
        },
        {
          name: "Ronald Richards",
          message: "Hola, buenos dias",
          avatarImage: "avatar-customer2",
          isOnline: false,
          iconPlatform: "messenger",
          active: false,
        },
        {
          name: "Jane Cooper",
          message: "He tenido problemas con mi conexión ...",
          avatarImage: "avatar-customer3",
          isOnline: false,
          iconPlatform: "telegram",
          active: false,
        },
      ],
    };
  },

  components: {
    ChatListItem,
    InputSearch,
  },
};
</script>

<style lang="scss" scoped>
.chatlist {
  border: 1px solid #f3f6fd;
  grid-area: chatlist;
  width: 320px;

  &__search {
    padding: 8px 16px;
  }
}
</style>
