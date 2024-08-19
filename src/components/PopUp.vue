<template>
  <div>
    <div
      class="fixed max-z-index top-0 bottom-0 left-0 right-0 px-6 py-3 flex flex-col"
    >
      <img class="background" src="/src/assets/images/popUp.jpg" />

      <div class="flex flex-col items-center gap-3 max-z-index">
        <h4 class="f-12-global mt-2 font-bold text-center text-white my-1">
          Title
        </h4>
        <h3 class="text-white whitespace-nowrap font-bold my-2 text-xl">
          Name Here
        </h3>
        <h3 class="text-white whitespace-nowrap font-bold my-2 text-xl">
          Date Here
        </h3>
        <button
          class="bg-transparent text-white border-b-2 border-solid border-green-500 rounded-md px-4 py-2 w-4/5"
          @click="OpenUndangan"
        >
          Buka Undangan
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    OpenUndangan() {
      // use router
    },
  },
};
</script>

<style scoped>
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
