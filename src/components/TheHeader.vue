<template>
  <header class="header">
    <div class="header__fd_row container">
      <div class="header__top">
        <a href="#"
          ><img src="../assets/images/logo.png" alt="Logo" class="header__logo"
        /></a>
        <button class="header__burger-btn" @click="showMenu()">
          <span></span>
          <span></span>
          <span></span>
        </button>
      </div>
      <div
        class="header__burgerMenu"
        :class="this.showMobileMenu ? 'open-menu' : 'closed-menu'"
      >
        <ul class="header__navbar">
          <li class="header__navbar_link">
            <a href="#availability">Каталог</a>
          </li>
          <li class="header__navbar_link">
            <a href="#form-container">Расчет стоимости</a>
          </li>
          <li class="header__navbar_link"><a href="#partners">Партнеры</a></li>
          <li class="header__navbar_link"><a href="#reviews">Отзывы</a></li>
        </ul>
        <div class="header__contacts">
          <div class="header__contacts_city">
            <div class="header__contacts-marker">
              <img src="../assets/images/map-marker.svg" alt="Map marker" />
            </div>
            <div class="header__contacts_info">
              <b>Москва</b>
              <a href="#">Все города</a>
            </div>
          </div>
          <div class="header__contacts_phone">
            <div class="header__contacts-marker">
              <img src="../assets/images/phone.svg" alt="Phone marker" />
            </div>
            <div class="header__contacts_info">
              <a href="8-985-344-76-46" class="none-underline"
                ><b>8-985-344-76-46</b></a
              >
              <a href="#form-container">Заказать звонок</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      showMobileMenu: false,
    };
  },
  methods: {
    showMenu() {
      this.showMobileMenu = !this.showMobileMenu;
    },
  },
};
</script>
