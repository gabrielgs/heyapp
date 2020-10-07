<template>
  <div class="conversation-status">
    <span class="conversation-status__description"
      >Marcar conversación como:</span
    >
    <div class="conversation-status__list">
      <div class="conversation-status__action">
        <img src="@/assets/icons/clear-circle.svg" alt="Icon Finish" />
        <span>Terminada</span>
      </div>
      <div class="conversation-status__action">
        <img src="@/assets/icons/success-circle.svg" alt="Icon Success" />
        <span>Resuelta</span>
      </div>
      <div class="conversation-status__action">
        <img src="@/assets/icons/assigned-circle.svg" alt="Icon Assigned" />
        <span>Asignada</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ConversationStatus",
};
</script>

<style lang="scss" scoped>
.conversation-status {
  display: flex;
  flex-direction: column;
  align-items: center;

  &__description {
    font-size: 12px;
    margin-bottom: 16px;
  }

  &__list {
    display: flex;
  }

  &__action {
    display: flex;
    flex-direction: column;
    align-items: center;

    img {
      margin-bottom: 4px;
    }

    span {
      font-size: 12px;
    }

    &:nth-child(1),
    &:nth-child(2) {
      margin-right: 20px;
    }
  }
}
</style>
