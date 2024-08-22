<template>
    <div>
      <!-- Hero Slide Images -->
      <ImageSlide />
  
      <!-- CONTENT -->
      <div class="text-black gap-5 padding-content">
        <h3 class="text-heading-title">Kepada Yth.<br />Bapak/Ibu/Saudara/i</h3>
        <div style="font-size: 16px" class="my-5">Name Invitation</div>
        <h3 class="text-heading-title">
          Mohon maaf apabila ada kesalahan<br />penulisan nama dan gelar
        </h3>
        <img alt="bismillah" src="/src/assets/images/bismillah-1.png" />
        <div class="text-heading-title">
          <p>Assalamualaikum Warahmatullahi Wabarakatuh</p>
        </div>
        <div class="text-heading-title">
          <p>
            Maha suci Allah SWT yang menciptakan makhluk-Nya berpasang - pasangan,
            dengan memohon ridho-Nya, InsyaAllah kami akan melangsungkan
            pernikahan
          </p>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import ImageSlide from "./ImageSlide.vue";
  </script>
  
  <style scoped>
  .text-heading-title {
    font-size: 14px;
    margin: 20px 0px 20px 0px;
  }
  .padding-content {
    max-width: 1280px;
    margin: 0 auto;
    padding: 1rem;
    text-align: center;
  }
  </style>
  