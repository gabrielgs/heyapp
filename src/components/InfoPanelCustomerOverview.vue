<template>
  <figure class="customer__overview">
    <div class="customer__avatar">
      <img src="@/assets/avatar-customer.jpg" alt="avatar-customer" />
    </div>
    <figcaption class="customer__name">Jane Cooper</figcaption>
  </figure>
</template>

<script>
export default {
  name: "InfoPanelCustomerOverview",
};
</script>

<style lang="scss" scoped>
.customer__overview {
  display: flex;
  flex-direction: column;
  align-items: center;

  .customer__avatar {
    width: 96px;
    height: 96px;
    margin-bottom: 16px;

    img {
      width: 100%;
      border-radius: 50%;
    }
  }

  .customer__name {
    font-size: 24px;
  }
}
</style>
