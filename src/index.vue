<script setup>
import Audio from "./components/Audio.vue";
import PopUp from "./components/PopUp.vue";
import Header from "./components/Header.vue";
import CommonMaster from "./components/commonMaster.vue";
</script>

<template>
  <div>
    <!-- ADD HEADER -->
    <Header />

    <!-- CONTENT -->
    <CommonMaster />
    <!-- Pop UP Undangan -->
    <PopUp />

    <!-- Audio -->
    <Audio />
  </div>
</template>
