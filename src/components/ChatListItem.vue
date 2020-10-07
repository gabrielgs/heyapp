<template>
  <li class="chat-item">
    <div class="chat-item__avatar">
      <div class="chat-item__avatar-container">
        <img
          class="chat-item__avatar-image"
          src="@/assets/avatar-customer.jpg"
          alt="Avatar Cutomer"
        />
        <img
          class="chat-item__platform"
          src="@/assets/icons/whatsapp.svg"
          alt="icon-whatssapp"
        />
        <div class="chat-item__online"></div>
      </div>
    </div>
    <div class="chat-item__info">
      <div class="chat-item__info-container">
        <span class="chat-item__name">Jane Cooper</span>
        <span class="chat-item__date">hace 10 minutos</span>
      </div>
      <span class="chat-item__message"
        >Ya he realizado las recomendaciones ...</span
      >
    </div>
  </li>
</template>

<script>
export default {
  name: "ChatListItem",
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
    padding-right: 20px;
  }

  &__info-container {
    display: flex;
    justify-content: space-between;
  }

  &__name {
    font-weight: bold;
  }

  &__date {
    color: $secondary-text;
  }

  &__date,
  &__message {
    font-size: 12px;
  }
}
</style>
