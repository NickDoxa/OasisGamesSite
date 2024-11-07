<script setup lang="ts">
import Card from 'primevue/card';
import {computed} from "vue";

const props = defineProps<{
  title: string
  subtitle?: string
  text: string
  icon: string
}>()

const getIcon = computed(() => 'pi ' + props.icon)
</script>

<template>
  <div class="icon-card">
    <Card class="icon-card-content">
      <template #header>
        <i :class="getIcon" style="font-size: 2rem; padding-top: 1rem; color: var(--p-sky-400);"/>
      </template>
      <template #title>
        <span class="heading">{{title}}</span>
      </template>
      <template #subtitle v-if="subtitle">
        <i class="icon-card-subtitle heading">{{subtitle}}</i>
      </template>
      <template #content>
        <div class="icon-card-text">{{text}}</div>
      </template>
    </Card>
  </div>
</template>

<style scoped>
.icon-card {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 1rem;
  flex-direction: column;
  text-align: center;
  margin: auto;
}

.icon-card-content {
  width: 22rem;
  min-height: 20rem;
}

.icon-card-subtitle {
  color: var(--p-sky-200);
}

.icon-card-text {
  width: 90%;
  margin: auto;
  padding-top: 1rem;
  text-align: left;
  font-style: normal;
}

@media (max-width: 67.5rem) {
  .icon-card-content {
    min-height: 10rem;
    width: 80%;
  }
}
</style>
