<template>
  <div v-if="DummyData === true" class="dummy-mode">
    sedang menggunakan data contoh
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
</style>
