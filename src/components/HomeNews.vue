<template>
  <div class="home-news" id="top">
    <div class="news-stroke">
      <span><strong>Новости компании:</strong> c 22-28 августа пройдет международный военно-технический форум «АРМИЯ-2021»</span>
    </div>
    <div class="send-buttons">
      <a href="https://www.rusarmyexpo.ru/" target="_blank">
        <div class="button">
          <span>Открыть</span>
        </div>
      </a>
    </div>
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
  padding: 10px 150px;
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
    padding: 10px 100px;
  }
  .news-stroke {
    font-size: 1em;
  }
}
@media only screen and (max-width : 1536px) {}
@media only screen and (max-width : 1366px) {}
@media only screen and (max-width : 1280px) {}
@media only screen and (max-width : 1024px) {}
@media only screen and (max-width : 800px) {
  .home-news {
    display: none;
  }
}
@media only screen and (max-width : 768px) {}
@media only screen and (max-width : 600px) {}
@media only screen and (max-width : 533px) {}
@media only screen and (max-width : 360px) {}
@media only screen and (max-width : 320px) {}
@media only screen and (max-width : 240px) {}
@media only screen and (max-width : 176px) {}
</style>