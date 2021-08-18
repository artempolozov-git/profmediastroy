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
            <a href="mailto:denissham@yandex.ru">denissham@yandex.ru</a>
          </div>
          <div class="contacts" style="align-items: center">
            <img src="@/assets/icons/phone-white.svg">
            <a href="tel:+79778546928">+7 977 854 69 28</a>
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
  margin-top: 20px;
  font-size: 1.3em;
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
  width: 30px;
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
  width: 25px;
  margin-right: 10px;
}
.button:hover {
  opacity: 0.8;
}
@media only screen and (max-width : 1130px) {
  .footer-container {
    display: block;
    padding: 80px 80px;
    height: auto;
  }
  .logotype {
    text-align: center;
    font-size: 1.5em;
    margin-right: 0;
  }
  .copyright {
    text-align: center;
  }
  .contacts {
    justify-content: center;
    font-size: 1em;
  }
  .contacts > img {
    width: 25px;
  }
  .email-phone {
    margin-top: 40px;
  }
}
@media only screen and (max-width : 450px) {
  .footer-container {
    padding: 40px 40px;
  }
  .logotype {
    text-align: center;
    font-size: 1.2em;
  }
  .button {
    height: 55px;
    padding: 17px 21px;
  }
  .send-buttons {
    display: block;
  }
  .button > img {
    width: 20px;
  }
}
</style>