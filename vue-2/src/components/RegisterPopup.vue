<!-- eslint-disable prettier/prettier -->
<template>
    <div class="account">
        <h3 class="header__title">Genshin Impact <span>туториал</span></h3>
        <div class="wrapper">
            <div class="account__menu">
                <div class="account__menu-block" @click="showContent(1)">
                    <h3>Регистрация</h3>
                    <div class="account__card">
                        <p>Пройти регистрацию на сайте</p>
                    </div>
                </div>
                <div class="account__menu-block" @click="showContent(2)">
                    <h3>Войти</h3>
                    <div class="account__card">
                        <p>Войти в существующий аккаунт</p>
                    </div>
                </div>
                <div class="account__menu-block" @click="showContent(3)">
                    <h3>Восстановление аккаунта</h3>
                    <div class="account__card">
                        <p>Забыли пароль? Не расстраивайтесь, мы вам поможем!</p>
                    </div>
                </div>
            </div>
            <div class="account__content" v-if="this.menuStatus === '1'">
                <img src="../assets/img/HuTao1.png" alt="HuTao">
                <form>
                    <p class="account__content-title">Заполните данные для регистрации учётной записи!</p>
                    <input type="email" name="email" id="popup-name" placeholder="Логин">
                    <input type="password" name="password" id="popup-password" placeholder="Пароль">
                    <input type="number" name="age" id="popup-age" placeholder="Возраст">
                    <input type="submit" value="Зарегистрироваться" disabled>
                </form>
            </div>
            <div class="account__content" v-if="this.menuStatus === '2'">
                <img src="../assets/img/Tartaglia2.png" alt="Tartaglia">
                <form>
                    <p class="account__content-title">Заполните данные для входа в учётную запись!</p>
                    <input type="email" name="email" id="popup-name" placeholder="Логин">
                    <input type="password" name="password" id="popup-password" placeholder="Пароль">
                    <input type="submit" value="Войти" disabled>
                </form>
            </div>
            <div class="account__content" v-if="this.menuStatus === '3'">
                <img src="../assets/img/Aether1.png" alt="Aether">
                <form>
                    <p class="account__content-title">Укажите почту, на которую была создана учётная запись!</p>
                    <input type="email" name="email" id="popup-name" placeholder="Логин">
                    <input type="submit" value="Проверить почту" disabled>
                </form>
            </div>
        </div>
    </div>
</template>
<script>
export default {
  data() {
    return {
      menuStatus: "1",
    };
  },
  methods: {
    showContent(status) {
      this.menuStatus = `${status}`;
    },
  },
};
</script>
