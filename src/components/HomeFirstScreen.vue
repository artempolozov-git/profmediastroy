<template>
  <div class="home-first-screen">
    <div class="title">
      <div class="first-stroke">Аренда и продажа</div>
      <div class="second-stroke">выставочных стендов</div>
    </div>
    <!--<div class="send-buttons">
      <a href="" target="_blank">
        <div class="button">
          <span>Заказать</span>
        </div>
      </a>
    </div>!-->
    <div class="stand-visual">
      <img src="@/assets/icons/stand-visual.svg">
      <span>Пример визуализации выставочного стенда</span>
    </div>
  </div>
</template>

<script>
    export default {
        name: "HomeFirstScreen",
    }
</script>

<style scoped>
.home-first-screen {
  padding: 100px 200px;
}
.title {
  color: #ffffff;
  font-size: 5em;
  font-weight: bold;
  margin: 0;
}
.first-stroke {
  background-color: #0a2973;
  padding: 15px 40px;
  box-sizing: border-box;
  border-radius: 15px;
  width: 54%;
  text-align: center;
}
.second-stroke {
  position: relative;
  bottom: 25px;
  background-color: #0a2973;
  padding: 15px 40px;
  box-sizing: border-box;
  border-radius: 15px;
  width: 63%;
}
.send-buttons {
  display: flex;
}
.send-buttons > a {
  text-decoration: none;
}
.button {
  padding: 30px 80px;
  box-sizing: border-box;
  font-size: 3em;
  border-radius: 15px;
  font-weight: bold;
  color: #ffffff;
  background-color: #009ee1;
}
.button:hover {
  background-color: #066fba;
}
.stand-visual {
  margin-top: 100px;
  text-align: center;
  color: #c7c7c7;
}
</style>