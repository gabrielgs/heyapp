<template>
  <header class="header">
    <img src="@/assets/logo.svg" alt="logo hey!" />
    <div class="user">
      <div class="user__avatar">
        <img src="@/assets/avatar-user.jpg" alt="avatar user" />
      </div>
      <span class="user__name"> Julian Mendez </span>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style lang="scss" scoped>
.header {
  background: $primary;
  display: flex;
  align-items: center;
  grid-area: header;
  justify-content: space-between;
  width: 100%;
  padding: 10px 24px;

  &__avatar {
    display: flex;
    align-items: center;
  }

  .user {
    display: flex;
    align-items: center;

    &__avatar {
      margin-right: 12px;
      height: 40px;
      width: 40px;

      img {
        border-radius: 50%;
        width: 100%;
      }
    }

    &__name {
      color: $secondary-light;
    }
  }
}
</style>
