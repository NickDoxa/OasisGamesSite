<script setup lang="ts">
import Tabs from 'primevue/tabs';
import TabList from 'primevue/tablist';
import Tab from 'primevue/tab';
import TabPanels from 'primevue/tabpanels';
import TabPanel from 'primevue/tabpanel';
import PrivacyPolicy from "@/components/PrivacyPolicyPage.vue";
import GamesPage from "@/components/GamesPage.vue";
import ContactPage from "@/components/ContactPage.vue";
</script>

<template>
  <Tabs value="0" class="tabs-container">
    <TabList>
      <Tab value="0"><i class="pi pi-headphones" /> Games</Tab>
      <Tab value="1"><i class="pi pi-eye-slash" /> Privacy</Tab>
      <Tab value="2"><i class="pi pi-send" /> Contact</Tab>
    </TabList>
    <TabPanels>
      <TabPanel value="0">
        <GamesPage/>
      </TabPanel>
      <TabPanel value="1">
        <PrivacyPolicy/>
      </TabPanel>
      <TabPanel value="2">
        <ContactPage/>
      </TabPanel>
    </TabPanels>
  </Tabs>
</template>

<style scoped>
.tabs-container {
  width: 80%;
  padding: 2rem;
  margin: auto;
}

@media (max-width: 30.4rem) {
  .tabs-container {
    padding: 1.5rem 0 0;
    width: 90%;
  }
}

:deep(.p-tabpanels) {
  background-color: #18181b;
}

:deep(.p-tab) {
  background-color: #27272a;
}

:deep(.p-tablist-tab-list) {
  background-color: #18181b;
}

:deep(.p-tab-active) {
  background-color: #18181b;
}
</style>
