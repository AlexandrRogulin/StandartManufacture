<template>
  <div class="v-popup">
    <div class="v-popup__header">
      <span class="v-popup__title">{{ popupTitle }}</span>
      <span @click="closePopup" class="v-popup__close">&#10006;</span>
    </div>
    <div class="v-popup__content">
      <slot> </slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "v-popup",
  props: {
    popupTitle: {
        type: String,
        default: "Product name"
    }
  },
  data() {
    return {};
  },
  methods: {
    closePopup() {
      this.$emit("closePopup");
    },
  },
};
</script>

<style scoped>
.v-popup {
  padding: 16px;
  position: fixed;
  top: 100px;
  right: 30%;
  width: 640px;
  border: 1px solid gray;
  z-index: 10;
  background: white;
}
.v-popup__header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.v-popup__close {
  cursor: pointer;
}
.v-popup__title {
  font-size: 20px;
  padding-bottom: 5px;
  font-weight: 700;
}
.v-popup__content {
  display: flex;
  justify-content: space-between;
}

@media screen and (max-width: 1000px) {
  .v-popup {
    right: 0;
    width: 100%;
  }
}

@media screen and (max-width: 576px) {
  .v-popup__content {
    display: flex;
    flex-direction: column;
  }
}
</style>
