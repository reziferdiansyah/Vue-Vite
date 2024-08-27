<template>
  <div>
    <div v-if="DummyData === true" class="dummy-mode">
      sedang menggunakan data contoh
    </div>
    <div class="music-control">
      <audio controls autoplay style="margin-top: -5px">
        <source src="/src/assets/images/audiostatic.mp3" type="audio/mpeg" />
        Your browser does not support the audio tag.
      </audio>
    </div>
    <!-- CONTENT MAIN -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      DummyData: true,
    };
  },
};
</script>

<style scoped>
.dummy-mode {
  position: fixed;
  z-index: 99;
  background: rgba(0, 0, 0, 0.3);
  padding: 5px 15px;
  color: #fff;
  border-radius: 50px;
  left: 10px;
  top: 10px;
  font-size: 10px;
}
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
