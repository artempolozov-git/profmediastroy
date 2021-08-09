<template>
  <div class="header">
    <div class="header-logotype">ГК «ПрофМедиаСтрой»</div>
    <div class="header-links">
      <span>Услуги</span>
      <span>Портфолио</span>
      <span>О нас</span>
      <span>Контакты</span>
    </div>
    <div class="send-buttons">
      <a href="mailto:denissham@yandex.ru" class="email-button">
        <div class="button">
          <img src="@/assets/icons/message.svg">
          <span>Написать</span>
        </div>
      </a>
      <a href="tel:+79778546928" class="phone-button">
        <div class="button" id="phone">
          <img src="@/assets/icons/phone-button.svg">
          <span>Позвонить</span>
        </div>
      </a>
    </div>
  </div>
</template>

<script>
    export default {
        name: "Header"
    }
</script>

<style scoped>
.header {
  display: flex;
  align-items: center;
  width: 100vw;
  height: 20vh;
  padding: 50px 200px;
  box-sizing: border-box;
}
.header-logotype {
  padding: 10px 30px;
  margin-right: 30px;
  box-sizing: border-box;
  font-size: 1.5vw;
  text-align: center;
  color: white;
  font-weight: normal;
  background-color: #066fba;
}
.header-logotype:hover {
  background-color: #0658a4;
  cursor: pointer;
}
.header-links > span {
  color: #2c2c2c;
  margin-right: 30px;
  font-weight: normal;
}
.header-links > span:hover {
  color: #009ee1;
  cursor: pointer;
}
.send-buttons {
  display: flex;
  justify-content: center;
  margin-left: auto;
}
.email-button {
  text-decoration: none;
}
.phone-button {
  text-decoration: none;
  margin-left: 30px;
}
.button {
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #009ee1;
  border-radius: 50px;
  height: 55px;
  box-sizing: border-box;
  padding: 10px 30px;
}
.button:hover {
  background-color: #066fba;
}
.button > span {
  font-weight: bold;
  color: white;
}
.button > img {
  width: 1.5vw;
  margin-right: 10px;
}
#phone {
  background-color: #00ad3a;
}
#phone:hover {
  background-color: #008b2f;
}
</style>