<template>
  <header class="header" v-if="registered === true">
    <div class="wrapper">
      <h3 class="header__title">Genshin Impact <span>туториал</span></h3>
      <p>Lorem ipsum dolor sit.</p>
      <div class="header__burger">
        <p>Меню</p>
        <ul class="header__list">
          <li class="header__list-item"><a href="#!">Главная</a></li>
          <li class="header__list-item"><a href="#!">Артефакты</a></li>
          <li class="header__list-item"><a href="#!">Персонажи</a></li>
        </ul>
      </div>
      <p>С возвращением, {{ this.userAccount.nickname }}!</p>
    </div>
  </header>
  <register-popup v-else></register-popup>
</template>

<script>
import { userData } from "../userData";
import RegisterPopup from "./RegisterPopup.vue";
export default {
  components: {
    RegisterPopup,
  },
  data() {
    return {
      userAccount: {},
      registered: false,
    };
  },
  created() {
    this.userAccount = userData;
  },
};
</script>
