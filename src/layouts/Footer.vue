<template>
  <div class="footer-container">
    <div class="footer-logotype">
      <div class="logotype">ГК «ПрофМедиаСтрой»</div>
      <div class="copyright">©2021 ПрофМедиаСтрой</div>
    </div>
    <div class="footer-contacts">
      <div>
        <div class="email-phone">
          <div class="contacts" style="align-items: center">
            <img src="@/assets/icons/email-white.svg">
            <a href="mailto:verhotour@gmail.com">denissham@yandex.ru</a>
          </div>
          <div class="contacts" style="align-items: center">
            <img src="@/assets/icons/phone-white.svg">
            <a href="tel:+79818595479">+7 981 859 54 79</a>
          </div>
        </div>
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
  </div>
</template>

<script>
    export default {
        name: "Footer"
    }
</script>

<style scoped>
.footer-container {
  display: flex;
  align-items: center;
  width: 100%;
  height: 350px;
  padding: 100px 150px;
  box-sizing: border-box;
  background-color: #0d1430;
}
.logotype {
  margin-right: 50px;
  font-size: 2em;
  color: #ffffff;
  font-weight: bold;
  user-select: none;
}
.footer-contacts {
  margin-left: auto;
}
.copyright {
  margin-top: 10px;
  color: #c7c7c7;
}
.contacts {
  display: flex;
  align-items: flex-start;
  width: 90%;
  margin-top: 20px;
  font-size: 1.2vw;
  color: #4c4c4c;
}
.contacts > a {
  text-decoration: none;
  color: #ffffff;
}
.contacts > a:hover {
  opacity: 0.8;
  cursor: pointer;
}
.contacts > img {
  width: 1.5vw;
  margin-right: 10px;
}
.send-buttons {
  display: flex;
  justify-content: center;
  margin-top: 30px;
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
  color: #ffffff;
  background-color: transparent;
  border: 3px solid #afafaf;
  border-radius: 50px;
  height: 60px;
  box-sizing: border-box;
  padding: 10px 30px;
}
.button > span {
  font-weight: normal;
  color: white;
}
.button > img {
  width: 1.5vw;
  margin-right: 10px;
}
.button:hover {
  opacity: 0.8;
}
</style>