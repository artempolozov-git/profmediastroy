<template>
  <div class="home-contacts-container" id="contacts">
    <div class="contacts-info">
      <div class="contacts-wrapper">
        <div class="title">Контакты</div>
        <div class="contacts">
          <img src="@/assets/icons/location.svg">
          <a href="https://yandex.ru/maps/21641/lobnja/house/krasnopolyanskaya_ulitsa_35/Z04YcgZlSEcPQFtsfXxzc35qZw==/?ll=37.415128%2C56.022293&z=16.65" target="_blank">Московская обл., г. Лобня, ул. Краснополянская, стр. 35</a>
        </div>
        <div class="contacts" style="align-items: center">
          <img src="@/assets/icons/email.svg">
          <a href="denissham@yandex.ru">denissham@yandex.ru</a>
        </div>
        <div class="contacts" style="align-items: center">
          <img src="@/assets/icons/phone.svg">
          <a href="tel:+79778546928">+7 977 854 69 28</a>
        </div>
        <div class="send-buttons">
          <a href="mailto:denissham@yandex.ru" class="email-button">
            <div class="button">
              <img src="@/assets/icons/message.svg">
              <span>Написать</span>
            </div>
          </a>
        </div>
      </div>
      <div class="contacts-map">
        <iframe class="map" src="https://yandex.ru/map-widget/v1/?um=constructor%3A0fb496afe65aca5a9e00b4379abc3254f864068d59a5133d1c038b3ac75c05db&amp;source=constructor" frameborder="0"></iframe>
      </div>
    </div>
  </div>
</template>

<script>
    export default {
        name: "HomeContacts"
    }
</script>

<style scoped>
.contacts-info {
  display: flex;
  align-items: center;
}
.contacts-wrapper {
  padding: 100px 0px 100px 150px;
  box-sizing: border-box;
}
.title {
  font-size: 2.5em;
  font-weight: bold;
  color: #212121;
}
.contacts {
  display: flex;
  align-items: flex-start;
  width: 90%;
  margin-top: 30px;
  font-size: 1.5em;
  color: #4c4c4c;
}
.contacts > a {
  text-decoration: none;
  color: #2c2c2c;
}
.contacts > a:hover {
  color: #d70a1f;
  box-sizing: border-box;
  cursor: pointer;
}
.contacts > img {
  width: 35px;
  margin-right: 10px;
}
.contacts-map {
  margin-left: auto;
}
.map {
  width: 900px;
  height: 600px;
}
.send-buttons {
  display: flex;
  margin-top: 50px;
}
.email-button {
  text-decoration: none;
}
.button {
  display: flex;
  align-items: center;
  justify-content: center;
  color: #ffffff;
  background-color: #b80a1e;
  border-radius: 50px;
  height: 70px;
  box-sizing: border-box;
  padding: 20px 40px;
}
.button > span {
  font-weight: normal;
  font-size: 1.3em;
  color: white;
}
.button > img {
  width: 25px;
  margin-right: 10px;
}
.button:hover {
  background-color: #d70a1f;
}
@media only screen and (max-width : 1890px) {
  .title {
    font-size: 2em;
  }
  .button > span {
    font-size: 1em;
  }
}
@media only screen and (max-width : 1680px) {
  .map {
    width: 750px;
  }
}
@media only screen and (max-width : 1540px) {
  .contacts-wrapper {
    padding: 100px 0px 100px 100px;
  }
  .map {
    width: 700px;
    height: 500px;
  }
}
@media only screen and (max-width : 1540px) {
  .map {
    height: 550px;
  }
  .contacts {
    font-size: 1.3em;
  }
}
@media only screen and (max-width : 1370px) {
  .contacts-wrapper {
    padding: 80px 0 80px 80px;
  }
  .map {
    width: 600px;
    height: 530px;
  }
}
@media only screen and (max-width : 1024px) {
  .map {
    width: 500px;
    height: 400px;
  }
  .contacts {
    font-size: 1em;
  }
  .contacts > img {
    width: 25px;
  }
  .button {
    padding: 20px 30px;
  }
}
@media only screen and (max-width : 800px) {
  .map {
    display: none;
  }
  .contacts-wrapper {
    padding: 50px 50px;
    margin: auto;
  }
  .send-buttons {
    display: flex;
    margin-top: 30px;
  }
  .contacts {
    margin-top: 15px;
    width: 100%;
  }
}
@media only screen and (max-width : 600px) {
  .title {
    font-size: 24px;
  }
}
@media only screen and (max-width : 360px) {
  .contacts-wrapper {
    padding: 40px 40px;
  }
}
</style>