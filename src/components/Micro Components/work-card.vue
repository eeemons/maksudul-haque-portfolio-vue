<script>
import ModalItem from "./modal-item.vue";

export default {
  data() {
    return {
      modalShow: false,
    };
  },
  methods: {
    toggleModalShow() {
      this.modalShow = true;
    },
  },
  components: { ModalItem },
};
</script>
<template>
  <div class="card-container">
    <div class="img-container"></div>
    <div class="button-grp">
      <button>Live Demo</button>
      <ModalItem />
    </div>
  </div>
</template>
<style scoped>
.card-container {
  width: 215px;
  height: 250px;
  border: 1px solid #707070;
  position: relative;
}
.img-container {
  width: 152px;
  height: 93px;
  border: 1px solid #707070;
  margin: 20px auto;
}

.button-grp {
  display: flex;
  align-items: center;
  justify-content: space-around;
  width: 100%;
  position: absolute;
  bottom: 0;
}

.button-grp button {
  border: 1px solid black;
  padding: 8px;
  margin-bottom: 10px;
  outline: none;
  color: #707070;
  text-align: center;
  text-decoration: none;
  background-color: transparent;
  font-family: inherit;
  cursor: pointer;
}

.button-grp button:hover {
  color: red;
}
</style>
