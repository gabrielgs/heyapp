<template>
  <header class="message-header">
    <div class="message-customer">
      <div class="message-customer__avatar">
        <img src="@/assets/avatar-customer.jpg" alt="avatar user">
      </div>
      <span class="message-customer__name">Jane Cooper</span>
    </div>
    <img class="info__icon" src="@/assets/icons/info.svg" alt="icon info">
  </header>
</template>

<script>
export default {
  name: "MessageHeader",
}
</script>

<style lang="scss" scoped>
  .message-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 12px 16px;

    .message-customer {
      display: flex;
      align-items: center;

      &__avatar {
        height: 32px;
        margin-right: 8px;
        width: 32px;

        img {
          border-radius: 50%;
          width: 100%;
        }
      }

      &__name {
        font-weight: bold;
      }
    }


    .info__icon {
      cursor: pointer;
    }
  }
</style>