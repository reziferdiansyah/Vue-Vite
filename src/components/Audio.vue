<template>
  <div class="music-control">
    <audio controls autoplay style="margin-top: -10px">
      <source src="/src/assets/images/audiostatic.mp3" type="audio/mpeg" />
      Your browser does not support the audio tag.
    </audio>
  </div>
</template>

<style scoped>
.music-control {
  width: 35px;
  height: 35px;
  position: fixed;
  z-index: 99;
  right: 10px;
  top: 10px;
  border-radius: 50%;
  padding-top: 8px;
}
</style>
