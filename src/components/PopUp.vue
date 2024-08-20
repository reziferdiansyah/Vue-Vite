<template>
  <div v-if="PopUpData === true">
    <div
      class="fixed max-z-index top-0 bottom-0 left-0 right-0 px-6 py-3 flex flex-col"
    >
      <img class="background" src="/src/assets/images/popUp.jpg" />
      <div class="flex flex-col items-center gap-5 max-z-index">
        <!-- Name Information -->
        <h3
          class="text-white whitespace-nowrap font-bold my-2 text-xl text-main"
        >
          Rizki & Rizka
        </h3>
        <!-- Date -->
        <span style="animation-delay: 1.3s">
          {{ DateOneNextMonth }}
        </span>
        <!-- Invitation to  -->
        <div>
          <p>Undangan Spesial Untuk</p>
          <p>Bapak/Ibu/Sahabat:</p>
        </div>
        <!-- Name Invitation -->
        <div>Name Invitation</div>
        <!-- Button Open -->
        <button
          class="bg-transparent mt-10 text-white border-b-1 border-solid border-white rounded-md px-4 py-2 w-3/5"
          style="border-radius: 20px"
          @click="OpenUndangan"
        >
          Buka Undangan
        </button>
        <!-- Text Info -->
        <div>Mohon maaf apabila ada kesalahan penulisan nama/gelar</div>
      </div>
    </div>
  </div>
</template>

<script>
import moments from "moment";

export default {
  data() {
    // Today Date Now
    const date = new Date();
    // Get the date + One months on Now
    const OneMonthsAfterDateNow = new Date(date);
    OneMonthsAfterDateNow.setMonth(date.getMonth() + 1);
    const afterOneMont = moments(OneMonthsAfterDateNow).format("DD MMMM YYYY");

    return {
      DateOneNextMonth: afterOneMont,
      PopUpData: true,
    };
  },

  methods: {
    OpenUndangan() {
      this.PopUpData = false;
    },
  },
};
</script>

<style scoped>
.text-main {
  font-size: 2.8rem;
  font-family: pacifico;
  line-height: 35px;
}
img.background {
  position: absolute;
  left: 0px;
  top: 0px;
  z-index: 99999;
  width: 100%;
  height: 100%;
}
.max-z-index {
  justify-content: center;
  z-index: 100000;
}
</style>
