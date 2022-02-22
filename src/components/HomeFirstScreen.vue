<template>
  <div class="substrate-container">
    <div class="main-container">
      <div class="logotype">
        <img src="@/assets/icons/pms-logo-white.svg">
        <span>ГК «ПрофМедиаСтрой»</span>
      </div>
      <h1 class="title">Аренда и продажа<br>выставочных стендов</h1>
      <div class="contacts">
        <div class="email">
          <img src="@/assets/icons/email-blue.svg">
          <a href="mailto:profmediastroy@bk.ru">profmediastroy@bk.ru</a>
        </div>
        <div class="phone">
          <img src="@/assets/icons/phone-blue.svg">
          <a href="tel:+74953690672">+7 (495) 369-06-72</a>
        </div>
      </div>
      <div class="send-buttons">
        <a href="mailto:profmediastroy@bk.ru" class="email-button">
          <div class="button">
            <img src="@/assets/icons/message.svg">
            <span>Написать</span>
          </div>
        </a>
        <a href="tel:+74953690672" class="phone-button">
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
    height: auto;
    padding: 100px 150px;
    box-sizing: border-box;
    background: url(../assets/images/background.webp);
    background-size: cover;
    background-position: center;
  }
  .main-container {
    width: 100%;
  }
  .logotype {
    display: flex;
    align-items: center;
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
  .logotype > img {
    width: 50px;
    margin-right: 15px;
  }
  .title {
    font-size: 5vw;
    color: white;
    text-align: center;
    font-weight: bold;
    text-transform: uppercase;
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
    font-size: 1.3em;
    font-weight: bold;
    color: white;
  }
  .button > img {
    width: 1.6vw;
    margin-right: 10px;
  }
  .button:hover {
    background-color: #00b1f5;
  }
  @media only screen and (max-width : 1890px) {
    .button > span {
      font-size: 1em;
    }
  }
  @media only screen and (max-width: 1367px) {
    .substrate-container {
      padding: 90px 80px;
    }
  }
  @media screen and (max-width: 800px) {
    .button {
      height: 50px;
      width: 10em;
      border-radius: 50px;
      box-sizing: border-box;
      padding: 10px 30px;
    }
    .substrate-container {
      padding: 90px 50px;
    }
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
      width: 20px;
    }
    .button > img {
      width: 20px;
    }
    @media screen and (max-width: 600px) {
      .logotype {
        padding: 15px 20px;
      }
      .logotype > img {
        width: 25px;
      }
      .substrate-container {
        padding: 70px 50px;
      }
    }
    @media screen and (max-width: 450px) {
      .substrate-container {
        padding: 70px 30px;
      }
    }
  }
</style>
