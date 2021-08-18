<template>
  <div class="portfolio-container" id="portfolio">
    <div class="portfolio-title">
      <div class="title"><span>Наши работы</span></div>
      <div class="description"><span>Объемные буквы, световые короба, печать на баннере «день-ночь», выставочные стенды</span></div>
    </div>
    <swiper class="swiper" :options="swiperOption">
      <swiper-slide>
        <div class="slide-1"></div>
      </swiper-slide>
      <swiper-slide>
        <div class="slide-2"></div>
      </swiper-slide>
      <swiper-slide>
        <div class="slide-3"></div>
      </swiper-slide>
      <swiper-slide>
        <div class="slide-4"></div>
      </swiper-slide>
      <swiper-slide>
        <div class="slide-5"></div>
      </swiper-slide>
      <swiper-slide>
        <div class="slide-6"></div>
      </swiper-slide>
      <swiper-slide>
        <div class="slide-7"></div>
      </swiper-slide>
      <swiper-slide>
        <div class="slide-8"></div>
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
      <div class="swiper-button-prev" slot="button-prev"></div>
      <div class="swiper-button-next" slot="button-next"></div>
    </swiper>
  </div>
</template>

<script>
    import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
    import 'swiper/css/swiper.css'
    export default {
        name: "HomePortfolio",
        data() {
            return {
                swiperOption: {
                    slidesPerView: 'auto',
                    spaceBetween: 30,
                    grabCursor: true,
                    loop: true,
                    pagination: {
                        el: '.swiper-pagination',
                        clickable: true
                    },
                    navigation: {
                        nextEl: '.swiper-button-next',
                        prevEl: '.swiper-button-prev'
                    }
                }
            }
        },
        components: {
            Swiper,
            SwiperSlide
        },
    }
</script>

<style scoped>
  .swiper-slide {
    width: 40%;
  }
  .swiper-slide:nth-child(2n) {
    width: 40%;
  }
  .swiper-slide:nth-child(3n) {
    width: 40%;
  }
.portfolio-container {
  padding: 100px 0 100px 150px;
  box-sizing: border-box;
}
.portfolio-title {
  margin-bottom: 30px;
}
.title {
  font-size: 2.5em;
  font-weight: bold;
  color: #212121;
}
.description {
  font-size: 1.3em;
  color: #4c4c4c;
}
.slide-1, .slide-2, .slide-3, .slide-4, .slide-5, .slide-6, .slide-7, .slide-8 {
  width: 100%;
  height: 600px;
}
.slide-1 {
  background-image: url(../assets/images/portfolio/squeen.webp);
  background-size: cover;
  background-position: top;
}
.slide-2 {
  background-image: url(../assets/images/portfolio/rgosh.webp);
  background-size: cover;
  background-position: center;
}
.slide-3 {
  background-image: url(../assets/images/portfolio/redcube.webp);
  background-size: cover;
  background-position: top;
}
.slide-4 {
  background-image: url(../assets/images/portfolio/avitowork.webp);
  background-size: cover;
  background-position: center;
}
.slide-5 {
  background-image: url(../assets/images/portfolio/rivgosh.webp);
  background-size: cover;
  background-position: center;
}
.slide-6 {
  background-image: url(../assets/images/portfolio/bahetle.webp);
  background-size: cover;
  background-position: center;
}
.slide-7 {
  background-image: url(../assets/images/portfolio/wdog.webp);
  background-size: cover;
  background-position: center;
}
.slide-8 {
  background-image: url(../assets/images/portfolio/megafon.webp);
  background-size: cover;
  background-position: top;
}
@media only screen and (max-width : 1890px) {
  .portfolio-container {
    padding: 100px 0 100px 100px;
  }
  .title {
    font-size: 2em;
  }
  .description {
    font-size: 1em;
  }
}
@media only screen and (max-width : 1550px) {
  .slide-1, .slide-2, .slide-3, .slide-4, .slide-5, .slide-6, .slide-7, .slide-8 {
    width: 100%;
    height: 500px;
  }
}
@media only screen and (max-width : 1280px) {
  .portfolio-container {
    padding: 80px 0 80px 80px;
  }
  .slide-1, .slide-2, .slide-3, .slide-4, .slide-5, .slide-6, .slide-7, .slide-8 {
    height: 450px;
  }
}
@media only screen and (max-width : 1024px) {
  .slide-1, .slide-2, .slide-3, .slide-4, .slide-5, .slide-6, .slide-7, .slide-8 {
    height: 400px;
  }
  .swiper-slide {
    width: 50%;
  }
  .swiper-slide:nth-child(2n) {
    width: 50%;
  }
  .swiper-slide:nth-child(3n) {
    width: 50%;
  }
}
@media only screen and (max-width : 800px) {
  .portfolio-container {
    padding: 50px 0;
  }
  .portfolio-title {
    margin: 0 0 30px 80px;
  }
  .slide-1, .slide-2, .slide-3, .slide-4, .slide-5, .slide-6, .slide-7, .slide-8 {
    height: 350px;
  }
  .swiper-slide {
    width: 60%;
  }
  .swiper-slide:nth-child(2n) {
    width: 60%;
  }
  .swiper-slide:nth-child(3n) {
    width: 60%;
  }
}
@media only screen and (max-width : 600px) {
  .portfolio-container {
    padding: 40px 0;
  }
  .portfolio-title {
    margin: 0 0 30px 40px;
  }
  .title {
    font-size: 24px;
  }
  .swiper-slide {
    width: 80%;
  }
  .swiper-slide:nth-child(2n) {
    width: 80%;
  }
  .swiper-slide:nth-child(3n) {
    width: 80%;
  }
}
@media only screen and (max-width : 361px) {
  .slide-1, .slide-2, .slide-3, .slide-4, .slide-5, .slide-6, .slide-7, .slide-8 {
    height: 300px;
  }
}
</style>