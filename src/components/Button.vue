<template>
  <button class="button">
    <img src="@/assets/icons/send.svg" alt="Icon Send" />
    Enviar
  </button>
</template>

<style lang="scss" scoped>
.button {
  display: flex;
  align-items: center;
  border: none;
  border-radius: 4px;
  background: $primary;
  color: $secondary-light;
  cursor: pointer;
  font-size: 16px;
  padding: 10px 16px;

  img {
    margin-right: 8px;
  }
}
</style>
