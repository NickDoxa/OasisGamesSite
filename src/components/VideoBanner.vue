<script setup lang="ts">

</script>

<template>
  <div class="video-banner">
    <video muted loop autoplay playsinline class="video-banner video-player">
      <source src="@/assets/videos/videobanner.mp4" type="video/mp4" />
    </video>
  </div>
</template>

<style scoped>
.video-banner {
  width: 100%;
  padding-bottom: 0;
  .video-player {
    border-bottom: black solid 0.2rem;
  }
}
</style>
