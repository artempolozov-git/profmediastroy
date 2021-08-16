<template>
  <div class="header">
    <div class="header-logotype">
      <span v-scroll-to="{el:'#top', offset: -150}">ГК «ПрофМедиаСтрой»</span>
    </div>
    <div class="header-links">
      <span v-scroll-to="{el:'#services', offset: -150}">Услуги</span>
      <span v-scroll-to="{el:'#portfolio', offset: -80}">Наши работы</span>
      <span v-scroll-to="{el:'#about-company', offset: -150}">О компании</span>
      <span v-scroll-to="{el:'#contacts', offset: -130}">Контакты</span>
    </div>
    <div class="send-buttons">
        <div class="button" @click="feedbackForm">
          <img src="@/assets/icons/buy.svg">
          <span>Заказать</span>
        </div>
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
        name: "Header",
        methods: {
            feedbackForm(){
                var form = document.getElementById("feedback");
                form.style.display = (form.style.display == 'none') ? 'block' : 'none'
            }
        },
    }
</script>

<style scoped>
.header {
  display: flex;
  align-items: center;
  position: sticky;
  z-index: 2;
  top: 0;
  width: 100%;
  max-width: 1920px;
  margin: auto;
  padding: 40px 150px;
  box-sizing: border-box;
  background-color: white;
  box-shadow: 0px 5px 5px -5px rgba(144, 144, 144, 0.7);
}
.header-logotype {
  margin-right: 50px;
  font-size: 2em;
  text-align: center;
  color: #0a2c87;
  font-weight: bold;
  user-select: none;
}
.header-logotype:hover {
  color: #0a34af;
  cursor: pointer;
}
.header-links > span {
  font-size: 1.3em;
  color: #2c2c2c;
  margin-right: 40px;
  user-select: none;
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
.phone-button {
  text-decoration: none;
  margin-left: 30px;
}
.button {
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #0a2c87;
  height: 60px;
  width: 13em;
  border-radius: 100px;
  box-sizing: border-box;
  padding: 10px 30px;
}
.button:hover {
  background-color: #0a37af;
  cursor: pointer;
}
.button > span {
  color: white;
  font-size: 1.3em;
}
.button > img {
  width: 1.5vw;
  margin-right: 10px;
}
#phone {
  background-color: #00ad3a;
}
#phone:hover {
  background-color: #00c43c;
}
</style>