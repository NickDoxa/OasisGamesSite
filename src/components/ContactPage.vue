<script setup lang="ts">
import Panel from 'primevue/panel';
import Button from 'primevue/button'
</script>

<template>
  <div class="contact-container" v-animateonscroll="{ enterClass: 'animate-fadein', leaveClass: 'animate-fadeout' }">
    <h1 class="heading">Contacts and Socials</h1>
    <Panel header="Contact">
      <p><span style="color: var(--p-sky-400)">Email:</span> nick@oasisgames.net</p>
      <p><span style="color: var(--p-sky-400)">Phone:</span> +1 (813) 416-2706</p>
    </Panel>
    <Panel header="Social Media">
      <div class="social-buttons-container">
        <a href="https://discordapp.com/users/492105960912060438" target="_blank"><Button label="Discord" icon="pi pi-discord"/></a>
        <a href="https://instagram.com/oasisgamesofficial" target="_blank"><Button label="Instagram" icon="pi pi-instagram"/></a>
        <a href="https://www.youtube.com/@oasisgames13" target="_blank"><Button label="Youtube" icon="pi pi-youtube"/></a>
      </div>
    </Panel>
  </div>
</template>

<style scoped>
.contact-container {
  width: 90%;
  margin: auto;
  padding-top: 2rem;
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

.social-buttons-container {
  display: flex;
  align-items: center;
  justify-content: space-evenly;
  text-align: center;
  margin: auto;
}

@media (max-width: 45rem) {
  .social-buttons-container {
    flex-direction: column;
    gap: 2rem;
  }
}
</style>
