<template>
  <div class="substrate-container">
    <div class="main-container">
      <div class="logotype">ГК «ПрофМедиаСтрой»</div>
      <div class="title">Аренда и продажа<br>выставочных стендов</div>
      <div class="contacts">
        <div class="email">
          <img src="@/assets/icons/email-blue.svg">
          <a href="denissham@yandex.ru">denissham@yandex.ru</a>
        </div>
        <div class="phone">
          <img src="@/assets/icons/phone-blue.svg">
          <a href="tel:+79778546928">+7 977 854 69 28</a>
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
          <div class="button">
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
        name: 'HelloWorld',
    }
</script>

<style scoped>
  .substrate-container {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    height: 100vh;
    box-sizing: border-box;
    background: url(../assets/images/background.webp);
    background-size: cover;
    background-position: center;
  }
  .main-container {
    width: 100%;
  }
  .logotype {
    width: max-content;
    padding: 25px;
    box-sizing: border-box;
    margin: auto;
    font-size: 2vw;
    font-weight: bold;
    text-align: center;
    color: white;
    background-color: #0a2c87;
  }
  .title {
    font-size: 5vw;
    color: white;
    text-align: center;
    width: 70%;
    font-weight: bold;
    text-transform: uppercase;
    margin: 50px auto 0;
  }
  .contacts {
    display: flex;
    justify-content: center;
    margin-top: 50px;
  }
  .email {
    display: flex;
    align-items: center;
    font-size: 2vw;
    color: white;
    font-weight: bold;
  }
  .phone {
    display: flex;
    align-items: center;
    font-size: 2vw;
    color: white;
    font-weight: bold;
    margin-left: 50px;
  }
  .email:hover, .phone:hover {
    opacity: 0.8;
  }
  .phone > a, .email > a {
    text-decoration: none;
    color: #ffffff;
  }
  .email > img, .phone > img {
    width: 2.5vw;
    margin-right: 10px;
  }
  .send-buttons {
    display: flex;
    justify-content: center;
    margin-top: 50px;
  }
  .email-button {
    text-decoration: none;
  }
  .phone-button {
    text-decoration: none;
    margin-left: 50px;
  }
  .button {
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: #009ee1;
    border-radius: 50px;
    width: max-content;
    box-sizing: border-box;
    padding: 20px 30px;
  }
  .button > span {
    font-size: 1.5vw;
    font-weight: bold;
    color: white;
  }
  .button > img {
    width: 1.6vw;
    margin-right: 10px;
  }
  .button:hover {
    background-color: #066fba;
  }
  @media screen and (max-width: 800px) {
    .logotype {
      font-size: 5vw;
    }
    .title {
      font-size: 9vw;
    }
    .phone {
      margin-left: 0;
      margin-top: 20px;
    }
    .contacts {
      display: block;
    }
    .phone-button {
      margin-left: 30px;
    }
    .email, .phone {
      font-size: 5vw;
      justify-content: center;
    }
    .email > img, .phone > img {
      width: 5vw;
    }
    .button > span {
      font-size: 4vw;
    }
    .button > img {
      width: 4vw;
    }
    @media screen and (max-width: 600px) {
      .substrate-container {
        height: 75vh;
      }
      .logotype {
        padding: 15px 20px;
      }
    }
    @media screen and (max-width: 450px) {
      .substrate-container {
        height: 60vh;
      }
    }
  }
</style>
