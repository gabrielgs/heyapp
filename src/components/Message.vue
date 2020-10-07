<template>
  <div :class="['message', isMessageIn ? 'message__in' : 'message__out']">
    <div class="message__container">
      <span class="message__text">
        {{ message }}
      </span>
      <div class="message__hour">
        <span>4:27 PM</span>
        <img
          v-if="!isMessageIn"
          src="@/assets/icons/read.svg"
          alt="Icon Read"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Message",
  props: {
    isMessageIn: {
      type: Boolean,
    },

    message: {
      type: String,
    },
  },
};
</script>

<style lang="scss" scoped>
.message {
  width: 100%;
  display: flex;
  margin-bottom: 32px;

  &__container {
    display: flex;
    flex-direction: column;
    max-width: 341px;
    padding: 16px 16px 4px;
  }

  &__hour {
    color: #e5e5e5;
    display: flex;
    justify-content: flex-end;
    font-size: 10px;

    span {
      margin-right: 4px;
    }
  }

  &__out {
    justify-content: flex-end;
    .message__container {
      color: $secondary-light;
      background: $primary;
      border-radius: 20px 20px 0 20px;
    }
    .message__hour {
      color: $secondary-text;
    }
  }

  &__in {
    justify-content: flex-start;
    .message__container {
      color: #000;
      background: $secondary;
      border-radius: 20px 20px 20px 0;
    }
    .message__hour {
      color: $secondary-text;
    }
  }
}
</style>
