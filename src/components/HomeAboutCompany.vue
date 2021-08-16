<template>
  <div class="home-about-container" id="about-company">
    <div class="about-title">
      <h1 class="title">О компании</h1>
      <p class="description">ГК «ПрофМедиаСтрой» предлагает вам проектирование, строительство и аренду
        выставочных стендов любой сложности с предоставлением оборудования
        и сопутствующих услуг в Москве и Московской области!
        Мы располагаем производственной базой с самым современным оборудованием
        и складскими помещениями, что позволяет нам оперативно и качественно решать
        любые вопросы наших заказчиков.

        <br>Монтаж выставочных стендов осуществляется квалифицированными монтажниками,
        имеющими многолетний опыт работы в выставочном строительстве. Работая на всех
        выставочных площадках, мы имеем четкое представление об их специфике и требованиях.
        Наша компания берет на себя все задачи связанные с подводом воды и электричества,
        обеспечением мебелью и бытовой техникой!</p>
    </div>
    <div class="send-buttons" @click="feedbackForm">
      <div class="button">
        <img src="@/assets/icons/buy.svg">
        <span>Заказать продукцию компании</span>
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
  width: 100%;
  height: 600px;
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
  height: 60px;
  box-sizing: border-box;
  padding: 10px 30px;
}
.button > span {
  font-weight: normal;
  font-size: 1.1em;
  color: white;
  user-select: none;
}
.button > img {
  width: 1.5vw;
  margin-right: 10px;
}
.button:hover {
  opacity: 0.8;
  cursor: pointer;
}
</style>