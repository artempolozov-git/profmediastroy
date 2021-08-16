<template>
  <div class="home-advantages-container">
    <div class="advantages-wrapper">
      <div class="advantage-container">
        <div class="advantage-img"><img src="@/assets/icons/brain.svg"></div>
        <div class="advantage-description">Выполнение работ<br>от идеи до воплощения!</div>
      </div>
      <div class="advantage-container-two">
        <div class="advantage-img"><img src="@/assets/icons/layers.svg"></div>
        <div class="advantage-description">Застройка стендов<br>любой сложности!</div>
      </div>
      <div class="advantage-container">
        <div class="advantage-img"><img src="@/assets/icons/hands.svg"></div>
        <div class="advantage-description">Предоставление<br>оборудования и услуг!</div>
      </div>
    </div>
  </div>
</template>

<script>
    export default {
        name: "HomeAdvantages"
    }
</script>

<style scoped>
.home-advantages-container {
  padding: 100px 150px;
  box-sizing: border-box;
}
.advantages-wrapper {
  display: flex;
}
.advantage-container {
  width: 33.33%;
}
.advantage-container-two {
  width: 33.33%;
  border-left: 3px solid #d7d7d7;
  border-right: 3px solid #d7d7d7;
  box-sizing: border-box;
}
.advantage-img {
  width: 9vw;
  margin: auto;
}
.advantage-description {
  font-size: 1.5em;
  font-weight: bold;
  color: #2c2c2c;
  text-align: center;
  margin-top: 10px;
}
</style>