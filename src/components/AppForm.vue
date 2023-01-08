<template>
  <div class="form-container container" id="form-container">
    <form action="#" enctype="text/plain" name="application-form" class="form">
      <fieldset class="form__fieldset">
        <legend><h2 class="form__title">ОСТАВИТЬ ЗАВЯВКУ</h2></legend>
        <p class="form__desc">НА РАСЧЕТ СТОИМОСТИ</p>
        <input
          type="tel"
          id="phone"
          name="phone"
          placeholder="Номер телефона"
          required
          class="form__input form__input-tel"
        />
        <input
          type="email"
          id="email"
          name="email"
          placeholder="E-mail"
          required
          class="form__input form__input-email"
        />
        <input type="submit" value="Заказать расчет цены" class="form__btn" />
        <!-- <label for="checkbox__form" class="form__conditions"
          ><input type="checkbox" value="agree" class="form__checkbox" id="checkbox__form" />
          Соглашаюсь с <a href="#">условиями передачи данных</a></label
        > -->
        <label class="checkbox checkbox__style">
          <input type="checkbox" />
          <div class="checkbox__checkmark"></div>
          <div class="checkbox__body">Соглашаюсь с <a href="#">условиями передачи данных</a></div>
        </label>
      </fieldset>
    </form>
  </div>
</template>
