<template>
  <div class="services-container" id="services">
    <div class="outdoor-block" @click="feedbackForm">
      <div>
        <div class="outdoor-title">
          <span>Наружная реклама</span>
        </div>
        <div class="block-description">
          <span>От полноцветного банера до объемных букв со светодиодной
                подсветкой, с использованием технологии «День-Ночь».
                Печать на баннерах шириной до 5,0м. и длиной до 50,0м.</span>
        </div>
      </div>
    </div>
    <div class="stand-block" @click="feedbackForm">
      <div>
        <div class="stand-title">
          <span>Выставочные стенды</span>
        </div>
        <div class="block-description">
          <span>Аренда выставочных стендов с возможностью приобретения. От 4м², ценой до 50 000₽/м².
            Проектирование, производство и монтаж стендов любой
                сложности! Ответственное хранение.</span>
        </div>
      </div>
    </div>
    <div class="polygraphy-block" @click="feedbackForm">
      <div>
        <div class="polygraphy-title">
          <span>Бизнес-полиграфия</span>
        </div>
        <div class="block-description">
          <span>От подарочной книги до издания справочников!
                <br>Корпоративные подарки и сувениры для партнеров,
                сотрудников, родственников и друзей!</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
    export default {
        name: "HomeServices",
        methods: {
            feedbackForm(){
                var form = document.getElementById("feedback");
                form.style.display = (form.style.display == 'none') ? 'block' : 'none'
            }
        },
    }
</script>

<style scoped>
.services-container {
  display: flex;
  justify-content: center;
}
.outdoor-block {
  display: flex;
  align-items: flex-end;
  width: 33.33%;
  height: 700px;
  padding: 50px 50px;
  box-sizing: border-box;
  background: url(../assets/images/outdoor-background.webp) center center;
  background-size: 100% 100%;
  background-position: center;
  overflow: hidden;
  transition: background-size .2s ease-in;
}
.stand-block {
  display: flex;
  align-items: flex-end;
  width: 33.33%;
  height: 700px;
  padding: 50px 50px;
  box-sizing: border-box;
  background: url(../assets/images/stand-background.webp);
  background-size: 100% 100%;
  background-position: center;
  overflow: hidden;
  transition: background-size .2s ease-in;
}
.polygraphy-block {
  display: flex;
  align-items: flex-end;
  width: 33.33%;
  height: 700px;
  padding: 50px 50px;
  box-sizing: border-box;
  background: url(../assets/images/polygraphy-background.webp);
  background-size: 100% 100%;
  background-position: center;
  overflow: hidden;
  transition: background-size .2s ease-in;
}
.outdoor-block:hover, .stand-block:hover, .polygraphy-block:hover {
  transition: background-size .2s ease-in;
  background-size: 105% 105%;
  cursor: pointer;
}
.outdoor-title {
  font-size: 1.5vw;
  font-weight: bold;
  color: #ffffff;
  background-color: #009ee1;
  text-align: center;
  padding: 10px 30px;
  box-sizing: border-box;
  width: max-content;
}
.stand-title {
  font-size: 1.5vw;
  font-weight: bold;
  color: #ffffff;
  background-color: #0a2973;
  text-align: center;
  padding: 10px 30px;
  box-sizing: border-box;
  width: max-content;
}
.polygraphy-title {
  font-size: 1.5vw;
  font-weight: bold;
  color: #ffffff;
  background-color: #bb0a1e;
  text-align: center;
  padding: 10px 30px;
  box-sizing: border-box;
  width: max-content;
}
.outdoor-block:hover .outdoor-title {
  transition: background-size .2s ease-in;
  background-color: #00b1f5;
}
.stand-block:hover .stand-title {
  transition: background-size .2s ease-in;
  background-color: #0b37af;
}
.polygraphy-block:hover .polygraphy-title {
  transition: background-size .2s ease-in;
  background-color: #d70a1f;
}
.block-description {
  font-size: 1.1em;
  color: #ffffff;
  margin-top: 15px;
}
@media only screen and (max-width : 1895px) {
  .block-description {
    font-size: 1em;
  }
}
@media only screen and (max-width : 1690px) {
  .polygraphy-block {
    padding: 69px 50px;
  }
  .outdoor-block, .stand-block, .polygraphy-block {
    height: 650px;
  }
}
@media only screen and (max-width : 1550px) {
  .outdoor-block, .stand-block, .polygraphy-block {
    height: 570px;
  }
}
@media only screen and (max-width : 1367px) {
  .outdoor-block, .stand-block, .polygraphy-block {
    height: 540px;
  }
  .polygraphy-block {
    padding: 50px 50px;
  }
}
@media only screen and (max-width : 1280px) {
  .outdoor-block, .stand-block, .polygraphy-block {
    height: 500px;
  }
  .outdoor-title, .stand-title, .polygraphy-title {
    font-size: 1.3vw;
  }
}
@media only screen and (max-width : 1025px) {
  .outdoor-block, .stand-block, .polygraphy-block {
    height: 400px;
    padding: 40px 20px;
  }
  .block-description {
    font-size: 14px;
  }
}
@media only screen and (max-width : 800px) {
  .block-description {
    display: none;
  }
  .outdoor-block, .stand-block, .polygraphy-block {
    width: 100%;
    background-size: cover;
    background-position: center;
    height: 400px;
  }
  .outdoor-block:hover, .stand-block:hover, .polygraphy-block:hover {
    background-size: cover;
  }
  .polygraphy-title, .stand-title, .outdoor-title  {
    font-weight: normal;
  }
}
@media only screen and (max-width : 768px) {
  .outdoor-block, .stand-block, .polygraphy-block {
    height: 350px;
  }
}
@media only screen and (max-width : 600px) {
  .services-container {
    display: block;
  }
  .block-description {
    display: block;
  }
  .polygraphy-title, .stand-title, .outdoor-title  {
    font-size: 21px;
  }
}
@media only screen and (max-width : 430px) {
  .polygraphy-title, .stand-title, .outdoor-title  {
    font-size: 18px;
  }
}
</style>