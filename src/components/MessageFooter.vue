<template>
  <footer class="message-footer">
    <div class="message-actions">
      <img class="emoji" src="@/assets/icons/emoji.svg" alt="icon emoji" />
      <img class="files" src="@/assets/icons/clip.svg" alt="icon files" />
    </div>
    <div class="message-text">
      <input type="text" placeholder="Escribe un mensaje" />
    </div>
    <Button />
  </footer>
</template>

<script>
import Button from "@/components/Button.vue";
export default {
  name: "MessageFooter",

  components: {
    Button,
  },
};
</script>

<style lang="scss" scoped>
.message-footer {
  display: flex;
  align-items: center;
  padding: 8px 16px;
}

.message-actions {
  height: 32px;
  margin-right: 10px;

  .emoji {
    margin-right: 16px;
  }
}

.message-text {
  flex-grow: 1;
  margin-right: 10px;

  input {
    background: $secondary;
    border: none;
    border-radius: 100px;
    font-size: 16px;
    padding: 10px 16px 11px;
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
