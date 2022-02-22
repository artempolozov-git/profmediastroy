<template>
  <div class="home-about-container" id="about-company">
    <div>
      <div class="about-title">
        <h1 class="title">О компании</h1>
        <p class="description">Мы работаем с 2011 года!
          <br>Предлагаем Вам застройку стендов любой сложности! Эксклюзивные стенды с правом выкупа. Аренда любого оборудования,
          используемого при проведении и презентации выставок, а так же аудио и видео аппаратуру.
          Наши специалисты помогут провести Вашу выставку на высочайшем уровне!
          Ждём Ваших вопросов по почте: profmediastroy@bk.ru или просто позвоните нам по телефону: +7 (495) 369 06 72!</p>
      </div>
      <div class="send-buttons" @click="feedbackForm">
        <div class="button">
          <img src="@/assets/icons/buy.svg">
          <span>Заказать продукцию компании</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
    export default {
        name: "HomeAboutCompany",
        methods: {
            feedbackForm(){
                var form = document.getElementById("feedback");
                form.style.display = (form.style.display == 'none') ? 'block' : 'none'
            }
        },
    }
</script>

<style scoped>
.home-about-container {
  display: flex;
  align-items: center;
  width: 100%;
  padding: 100px 150px;
  box-sizing: border-box;
  background: url(../assets/images/about-background.webp);
  background-size: cover;
  background-position: center;
}
.title {
  margin: 0;
  font-size: 2.5em;
  font-weight: bold;
  color: #ffffff;
}
.description {
  width: 50%;
  font-size: 1.1em;
  color: #ffffff;
}
.send-buttons {
  display: flex;
  margin-top: 30px;
}
.button {
  display: flex;
  align-items: center;
  justify-content: center;
  color: #ffffff;
  background-color: transparent;
  border: 3px solid #afafaf;
  border-radius: 50px;
  box-sizing: border-box;
  padding: 20px 30px;
}
.button > span {
  font-weight: normal;
  font-size: 1.1em;
  color: white;
  user-select: none;
}
.button > img {
  width: 25px;
  margin-right: 10px;
}
.button:hover {
  opacity: 0.8;
  cursor: pointer;
}
@media only screen and (max-width : 1890px) {
  .title {
    font-size: 2em;
  }
  .description {
    font-size: 1em;
  }
  .button > span {
    font-size: 1em;
  }
}
@media only screen and (max-width : 1537px) {
  .description {
    width: 60%;
  }
}
@media only screen and (max-width : 1367px) {
  .home-about-container {
    padding: 100px 100px;
  }
}
@media only screen and (max-width : 1367px) {
  .home-about-container {
    padding: 80px 80px;
  }
}
@media only screen and (max-width : 800px) {
  .home-about-container {
    height: auto;
    padding: 50px 50px;
  }
  #info-block-two {
    display: none;
  }
  .description {
    width: 75%;
  }
}
@media only screen and (max-width : 600px) {
  .home-about-container {
    padding: 40px 40px;
  }
  #info-block-two {
    display: none;
  }
  .description {
    width: 100%;
  }
  .title {
    font-size: 24px;
  }
}
@media only screen and (max-width : 380px) {
  .home-about-container {
    padding: 40px 40px;
  }
  .button > span {
    font-size: 0.7em;
  }
}
</style>