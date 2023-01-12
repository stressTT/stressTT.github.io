<template>
  <div>
    <button @click="isModalOpen = true" class="btnPrice">
      Расчет Стоимости
      <i class="fa-solid fa-caret-right iconPrice"></i>
    </button>

    <div v-if="isModalOpen" class="modal-bg">
      <div class="modal-1">click outside to close modal</div>
      <button @click="isModalOpen = false">x</button>
    </div>
  </div>
</template>

<style lang="less" scoped>
.btnPrice {
  margin-bottom: 70px;
  margin-top: 25px;
}
.modal-bg {
  position: fixed;
  z-index: 10;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;

  background: rgba(var(--black), 0.5);

  display: flex;
  justify-content: center;
  align-items: center;
  .modal-1 {
    position: relative;
    z-index: 1;
    background: rgba(255, 255, 255, 1);
    padding: 50px 100px;
    border-radius: 5px;
    box-shadow: 0px 10px 5px 2px rgba(0, 0, 0, 0.1);
  }
}
</style>
<script>
export default {
  data() {
    return {
      isModalOpen: true,
    };
  },
};
</script>
