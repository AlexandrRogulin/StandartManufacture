<template>
  <div class="availability" id="availability">
    <div class="availability__container container">
      <h2 class="availability__title">ВСЕГДА В НАЛИЧИИ</h2>
      <div class="availability__block">
        <div
          class="availability__item"
          v-for="availability in data"
          :key="availability.id"
        >
          <v-popup v-if="isPopupVisible" @closePopup="closeInfoPopup" :popupTitle="availability.title">
            <img
              :src="
                require(`../assets/images/availability/${availability.image}.jpg`)
              "
              :alt="availability.title"
            />
            <div class="availability__modal_info">
              {{ availability.desc }}
              <br>
            {{ availability.price }} руб/комп
          </div>
          </v-popup>

          <div class="availability__item_img">
            <img
              :src="
                require(`../assets/images/availability/${availability.image}.jpg`)
              "
              :alt="availability.title"
              @click="showPopupInfo"
            />
          </div>
          <div class="availability__item_title">
            {{ availability.title }}
          </div>
          <form class="availability__item_form">
            <div class="availability__item_form-left">
              <p class="availability__item_price">
                {{ availability.price }} руб/комп
              </p>
            </div>
            <fieldset
              class="availability__item_form-right availability__item_order"
            >
              <div class="available__item_order-block">
                <input
                  type="number"
                  min="0"
                  max="9999"
                  id="order"
                  placeholder="0"
                  class="availability__item_count"
                /><label for="order" class="availability__item_text"
                  >комп.</label
                >
              </div>
              <div class="availability__btn">
                <input
                  type="submit"
                  value="Заказать"
                  class="availability__btn_style"
                />
              </div>
            </fieldset>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import vPopup from "./popup/v-popup.vue";
export default {
  components: {
    vPopup,
  },
  props: {
    data: {
      type: Array,
      default: () => [],
    },
  },
  data() {
    return {
      isPopupVisible: false,
    };
  },
  methods: {
    showPopupInfo() {
      this.isPopupVisible = true;
    },
    closeInfoPopup() {
      this.isPopupVisible = false;
    },
  },
};
</script>
