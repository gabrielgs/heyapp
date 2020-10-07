<template>
  <aside>
    <CustomerOverview />
    <ConversationStatus />
  </aside>
</template>

<script>
import CustomerOverview from "@/components/InfoPanelCustomerOverview.vue";
import ConversationStatus from "@/components/InfoPanelConversationStatus.vue";
export default {
  name: "InfoPanel",
  components: {
    CustomerOverview,
    ConversationStatus,
  },
};
</script>
