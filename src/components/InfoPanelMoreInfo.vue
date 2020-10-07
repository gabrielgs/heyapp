<template>
  <div class="more-info__list">
    <div class="about">
      <div class="more-info__header">
        <span>Acerca </span>
        <img
          class="show"
          src="@/assets/icons/arrow_down.svg"
          alt="Icon arrow down"
        />
      </div>
      <div class="about__item">
        <span class="title">Telefono</span>
        <span class="subtitle">+525529395670</span>
      </div>
      <div class="about__item">
        <span class="title">Hora local</span>
        <span class="subtitle">6:20 PM</span>
      </div>
    </div>
    <div class="shared-files">
      <div class="more-info__header">
        <span>Documentos Compartidos</span>
        <img
          class="show"
          src="@/assets/icons/arrow_right.svg"
          alt="Icon arrow right"
        />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.more-info__list {
  padding: 0 16px;

  .show {
    cursor: pointer;
  }
}

.more-info__header {
  display: flex;
  justify-content: space-between;
  padding: 19px 0 18px;
}

.about {
  &__item {
    display: flex;
    color: $secondary-text;
    flex-direction: column;
    margin-bottom: 16px;

    .title {
      font-size: 14px;
      font-weight: bold;
      margin-bottom: 4px;
    }
  }
}
</style>
