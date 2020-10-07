<template>
  <aside class="info-panel">
    <div class="close-panel">
      <img src="@/assets/icons/close.svg" alt="Icon Close" />
    </div>
    <CustomerOverview />
    <ConversationStatus />
    <MoreInfo />
  </aside>
</template>

<script>
import CustomerOverview from "@/components/InfoPanelCustomerOverview.vue";
import ConversationStatus from "@/components/InfoPanelConversationStatus.vue";
import MoreInfo from "@/components/InfoPanelMoreInfo.vue";
export default {
  name: "InfoPanel",
  components: {
    CustomerOverview,
    ConversationStatus,
    MoreInfo,
  },
};
</script>

<style lang="scss" scoped>
.info-panel {
  border: 1px solid #f3f6fd;
}

.close-panel {
  display: flex;
  justify-content: flex-end;
  padding: 16px;

  img {
    cursor: pointer;
  }
}
</style>
