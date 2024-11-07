<script setup lang="ts">

import IconCard from "@/components/common/IconCard.vue";
</script>

<template>
  <div class="card-display" v-animateonscroll="{ enterClass: 'animate-fadein', leaveClass: 'animate-fadeout' }">
    <IconCard title="Reliably Built"
              text="Oasis Games is built on the principle of reliability and consistency. We are dedicated to making fun, quality games that are built to last. Engineering of the highest quality is our highest priority."
              icon="pi-code"/>
    <IconCard title="Stable Performance"
              text="Building a consistently stable game requires a consistently stable foundation. All of our games are powered by Unity Engine and run actively on the Unity Services framework."
              icon="pi-bolt"/>
    <IconCard title="Global Access"
              text="All of our games are available around the world and we are commited to making our games accessible to everyone! Our future plans include language translation and closed-captioning on all cut scenes!"
              icon="pi-globe"/>
  </div>
</template>

<style scoped>
.card-display {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  padding-top: 2rem;
}

@media(max-width: 67.5rem) {
  .card-display {
    grid-template-columns: 1fr;
    gap: 1rem;
  }
}
</style>
