<template>
  <div class="input-group">
    <span class="button-search">
      <img src="@/assets/icons/search.svg" alt="icon search" />
    </span>
    <input
      class="input__search"
      type="text"
      placeholder="Buscar personas, número ..."
    />
  </div>
</template>

<script>
export default {
  name: "InputSearch",
};
</script>

<style lang="scss" scoped>
.input-group {
  display: flex;
  align-content: center;

  .button-search {
    background: $secondary;
    cursor: pointer;
    display: flex;
    padding: 8px 8px 8px 16px;
    border-radius: 100px 0 0 100px;
  }

  .input__search {
    background: $secondary;
    border: none;
    border-radius: 0 100px 100px 0;
    font-size: 14px;
    padding: 11px 0px 12px;
    width: 100%;

    &:focus {
      outline: none;
    }

    &::placeholder {
      color: $secondary-text;
    }
  }
}
</style>
