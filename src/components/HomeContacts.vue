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
          <a href="mailto:verhotour@gmail.com">denissham@yandex.ru</a>
        </div>
        <div class="contacts" style="align-items: center">
          <img src="@/assets/icons/phone.svg">
          <a href="tel:+79818595479">+7 981 859 54 79</a>
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
        <div><iframe class="map" src="https://yandex.ru/map-widget/v1/?um=constructor%3A0fb496afe65aca5a9e00b4379abc3254f864068d59a5133d1c038b3ac75c05db&amp;source=constructor" frameborder="0"></iframe></div>
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
.home-contacts-container {
  padding: 0 0 0 150px;
  box-sizing: border-box;
}
.contacts-info {
  display: flex;
  align-items: center;
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
  font-size: 1.5vw;
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
  width: 2vw;
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
  margin-top: 30px;
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
  width: 1.5vw;
  margin-right: 10px;
}
.button:hover {
  background-color: #d70a1f;
}
</style>