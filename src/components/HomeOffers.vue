<template>
  <div class="home-offers-container">
    <div class="offers-wrapper">
      <div>
        <div class="title">Заказ продукции</div>
        <div class="description">Оставьте свои контакты и мы свяжемся с вами,
          <br>чтобы обсудить детали проекта и особенности будущего заказа!</div>

        <form id="feedback-form" action="" method="POST" class="form-container">
          <div class="input-container">
            <input name="Имя" type="text" placeholder="Имя" class="input-box" required>
            <masked-input v-model="phone" mask="\+\7 (111) 111 11-11" name="Телефон" type="text" placeholder="Телефон" class="input-box" required></masked-input>
          </div>
          <input type="submit" id="my-form-button" class="button" value="Отправить">
          <span class="status-complete" id="my-form-status"></span>
        </form>

      </div>
    </div>
  </div>
</template>

<script>
    import MaskedInput from 'vue-masked-input'
    export default {
        name: "HomeOffers",
        components: {
            MaskedInput
        }
    }
</script>

<style scoped>
.home-offers-container {
  display: flex;
  align-items: center;
  justify-content: flex-end;
  width: 100%;
  height: 400px;
  padding: 100px 150px;
  box-sizing: border-box;
  background: url(../assets/images/offers-background.webp);
  background-size: cover;
  background-position: bottom;
}
.offers-wrapper {

}
.title {
  font-size: 3em;
  color: #ffffff;
  font-weight: bold;
}
.description {
  font-size: 1.3em;
  color: #e2e2e2;
}
.form-container {
  display: flex;
  align-items: center;
  margin-top: 50px;
}
.input-box {
  width: 15vw;
  height: 50px;
  font-size: 1.3em;
  color: #ffffff;
  margin-right: 30px;
  font-family: PMS;
  font-weight: 500;
  background-color: transparent;
  outline: none;
  border: 0;
  border-bottom: 2px solid #afafaf;
}
.input-box:focus {
  border-bottom: 2px solid #ffffff;
}
.button {
  width: 10vw;
  height: 60px;
  font-size: 1.1em;
  font-weight: normal;
  font-family: PMS;
  color: #ffffff;
  background-color: transparent;
  border: 3px solid #afafaf;
  border-radius: 50px;
}
.button:hover {
  opacity: 0.8;
  cursor: pointer;
}
</style>