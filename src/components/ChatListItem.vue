<template>
  <li :class="['chat-item', {active: customer.active}]">
    <div class="chat-item__avatar">
      <div class="chat-item__avatar-container">
        <img
          class="chat-item__avatar-image"
          :src="require(`../assets/${customer.avatarImage}.jpg`)"
          alt="Avatar Cutomer"
        />
        <img
          class="chat-item__platform"
          :src="require(`../assets/icons/${customer.iconPlatform}.svg`)"
          alt="icon-whatssapp"
        />
        <div v-if="customer.isOnline" class="chat-item__online"></div>
      </div>
    </div>
    <div class="chat-item__info">
      <div class="chat-item__info-container">
        <span class="chat-item__name">{{ customer.name }}</span>
        <span class="chat-item__date">hace 10 minutos</span>
      </div>
      <span class="chat-item__message"
        >{{ customer.message }}</span
      >
    </div>
  </li>
</template>

<script>
export default {
  name: "ChatListItem",
  props: {
    customer: {
      type: Object,
    },
  },
};
</script>

<style lang="scss" scoped>
.chat-item {
  cursor: pointer;
  display: flex;
  align-items: center;
  padding: 8px 16px;
  transition: all 0.3s ease;

  &:hover,
  &.active {
    background: $secondary;
  }

  &__avatar {
    margin-right: 12px;
  }

  &__avatar-container {
    width: 56px;
    height: 56px;
    position: relative;
  }

  &__avatar-image {
    width: 100%;
    border-radius: 50%;
  }

  &__platform {
    position: absolute;
    bottom: 0;
    right: 0;
  }

  &__online {
    &::before {
      content: "";
      background: $success;
      border-radius: 50%;
      width: 8px;
      height: 8px;
      position: absolute;
      top: 2px;
      left: 8px;
    }
  }

  &__info {
    width: 100%;
  }

  &__info-container {
    display: flex;
    justify-content: space-between;
  }

  &__name {
    font-weight: 400;
  }

  &__date {
    color: $secondary-text;
  }

  &__date,
  &__message {
    font-size: 12px;
  }

  &__message {
    color: $secondary-text;
  }

  &.active {
    .chat-item__name {
      font-weight: bold;
    }

    .chat-item__message {
      color: #000;
    }
  }
}
</style>
