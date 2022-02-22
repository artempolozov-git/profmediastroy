<template>
  <div class="home-news" id="top">
    <div class="news-stroke">
      <span><strong>Новости компании:</strong> В рамках совместного проекта ГК «ПрофМедиаСтрой» и переплетная Мастерская «ЗОЛОТОЙ ВЕК» изготовили подарочное издание книги «Мировая история нефти и газа». К изданию планируется ещё одна книга.</span>
    </div>
    <!--<div class="send-buttons">
      <a href="https://www.rusarmyexpo.ru/" target="_blank">
        <div class="button">
          <span>Открыть</span>
        </div>
      </a>
    </div>!-->
  </div>
</template>

<script>
    export default {
        name: "HomeNews"
    }
</script>

<style scoped>
.home-news {
  display: flex;
  align-items: center;
  width: 100%;
  background-color: #009ee1;
  padding: 20px 150px;
  box-sizing: border-box;
}
.news-stroke {
  color: #ffffff;
  font-size: 1.3em;
}
.send-buttons {
  display: flex;
  justify-content: center;
  margin-left: auto;
}
.send-buttons > a {
  text-decoration: none;
}
.button {
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50px;
  border: 3px solid #ffffff;
  height: 45px;
  box-sizing: border-box;
  padding: 10px 30px;
  font-weight: bold;
  color: white;
}
.button:hover {
  opacity: 0.8;
}
@media only screen and (max-width : 1890px) {
  .home-news {
    padding: 20px 100px;
  }
  .news-stroke {
    font-size: 1em;
  }
}
@media only screen and (max-width : 800px) {
  .home-news {
    padding: 10px 30px;
  }
}
</style>