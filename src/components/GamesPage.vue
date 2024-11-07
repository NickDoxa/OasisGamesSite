<script setup lang="ts">
import Dialog from "primevue/dialog";
import Button from "primevue/button";
import {ref} from "vue";

const visible = ref<boolean>(false);
</script>

<template>
  <div class="tabs-game-panel" v-animateonscroll="{ enterClass: 'animate-fadein', leaveClass: 'animate-fadeout' }">
    <h1 class="heading">Toon Bot 2099</h1>
    <h2 class="heading sub">Steam - Multiplayer (free to play)</h2>
    <h3 class="heading" style="color: var(--p-sky-200)">Availability: <i class="pi pi-apple"/> MacOS, <i class="pi pi-microsoft"/> Windows</h3>
    <p class="tabs-body">
      Toon Bot 2099 is a multiplayer parkour game that incorporates strategy and combat into an action packed
      race for the finish! The goal is simple, get your gears to the end of the course and complete the objective!
      Be warned, other players can use their special abilities to try to stop you from getting to the end. However,
      using a special ability can also backfire and cause the user to potentially throw the game! Test your luck
      and compete against your friends in this Sci-Fi game!
    </p>
    <img alt="lobby view of Toon Bot 2099" src="/lobby.png" class="tabs-game-image"/>
    <Button label="Steam Download" size="large" icon="pi pi-download" class="tabs-download-button" @click="visible = true"/>
    <Dialog v-model:visible="visible" modal header="Not Released Yet!" :style="{ width: '25rem' }">
            <span class="text-surface-500 dark:text-surface-400 block mb-8">Toon Bot 2099 has not been released yet...
              Check back for a release date soon!</span>
    </Dialog>
  </div>
</template>

<style scoped>
.tabs-game-panel {
  padding: 2rem;
  display: flex;
  flex-direction: column;
  gap: 0.3rem;
}

.tabs-game-image {
  width: 60%;
  height: auto;
  text-align: center;
  margin: 1rem auto auto;
  border: 0.2rem solid;
  border-color: var(--p-sky-700)
}

.tabs-download-button {
  width: 18rem;
  margin: 1rem auto auto;
}

@media (max-width: 44.75rem) {
  .tabs-download-button {
    width: 13rem;
  }
}

@media (max-width: 36.875rem) {
  .heading {
    font-size: 0.9rem;
  }

  .tabs-body {
    font-size: 0.8rem;
  }

  .tabs-game-image {
    width: 100%;
  }
}
</style>
