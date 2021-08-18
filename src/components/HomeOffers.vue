<template>
  <div class="home-offers-container">
    <div class="offers-wrapper">
      <div>
        <div class="title">Заказ продукции</div>
        <div class="description">Оставьте свои контакты и мы свяжемся с вами,
          <br id="br-none">чтобы обсудить детали проекта и особенности будущего заказа!</div>

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
.title {
  font-size: 3em;
  color: #ffffff;
  font-weight: bold;
}
.description {
  font-size: 1.3em;
  margin-top: 10px;
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
@media only screen and (max-width : 1537px) {
  .title {
    font-size: 2em;
  }
  .description {
    font-size: 1em;
  }
  .input-box {
    font-size: 1em;
  }
  .button {
    font-size: 1em;
  }
}
@media only screen and (max-width : 1024px) {
  .home-offers-container {
    padding: 80px 80px;
    height: 350px;
  }
  .button {
    width: 15vw;
    height: 55px;
  }
}
@media only screen and (max-width : 800px) {
  .home-offers-container {
    padding: 50px 50px;
    height: 300px;
    background-size: auto;
  }
  .button {
    width: 17vw;
    height: 45px;
  }
  .input-box {
    width: 20vw;
    height: 40px;
  }
}
@media only screen and (max-width : 600px) {
  .form-container {
    display: block;
    margin-top: 0;
  }
  .home-offers-container {
    padding: 30px 30px;
    height: 450px;
  }
  .button {
    width: 25vw;
    font-size: 1em;
    margin-top: 30px;
  }
  .input-box {
    width: 80%;
    margin-top: 30px;
  }
}
@media only screen and (max-width : 460px) {
  .button {
    width: 35vw;
  }
  #br-none {
    display: none;
  }
}
</style>