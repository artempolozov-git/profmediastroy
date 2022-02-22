<template>
  <Slide right :closeOnNavigation="true" noOverlay>
    <span class="bm-cross-button cross-style" style="/* right: 250px; */"></span>
    <div class="links" v-scroll-to="{el:'#services', offset: -150}">Услуги</div>
    <div class="links" v-scroll-to="{el:'#portfolio', offset: -80}">Наши работы</div>
    <div class="links" v-scroll-to="{el:'#about-company', offset: -150}">О компании</div>
    <div class="links" v-scroll-to="{el:'#contacts', offset: -130}">Контакты</div>
    <div class="send-button-burger">
      <div class="button-burger" @click="feedbackForm">
        <img src="@/assets/icons/buy.svg">
        <span>Заказать</span>
      </div>
      <a href="tel:+79778546928" class="phone-button-burger">
        <div class="button-burger" id="phone-burger">
          <img src="@/assets/icons/phone-button.svg">
          <span>Позвонить</span>
        </div>
      </a>
    </div>
  </Slide>
</template>

<script>
    import { Slide } from 'vue-burger-menu'
    export default {
        name: "BurgerMenu",
        components: {
            Slide // Register your component
        },
        methods: {
            feedbackForm(){
                var form = document.getElementById("feedback");
                form.style.display = (form.style.display == 'none') ? 'block' : 'none'
            }
        },
    }
</script>

<style>
  .bm-burger-button {
    right: 80px;
    left: 0;
    top: 42px;
  }
  .bm-menu {
    background-color: white;
    box-shadow: 1px 1px 2px 1px #ccc;
  }
  .bm-cross {
    background: #212121;
  }
  .bm-item-list {
    color: #2c2c2c;
    font-weight: 500;
    margin-left: 10%;
    font-size: 1em;
    cursor: pointer;
    transition: color .1s ease-in;
  }
  .bm-item-list > div:hover {
    color: #374DFF;
    transition: color .2s ease-in;
  }
  .bm-item-list > * {
    display: block;
    text-decoration: none;
    padding: 16px;
    width: 15em;
  }
  .bm-item-list > * > span {
    margin-left: 10px;
    font-weight: 700;
    color: white;
  }
  .icon-burger > img {
    width: 40px;
    height: 40px;
    transition: opacity .2s ease-in;
  }
  .icon > span {
    font-size: 16px;
    color: #686868;
    margin-left: 5px;
    font-weight: 500;
  }
  .messengers-first > img {
    width: 2em;
    transition: opacity .2s ease-in;
  }
  .messengers-burger > img {
    margin-left: 25px;
    width: 2em;
    transition: opacity .2s ease-in;
  }
  .messengers-burger > span {
    font-size: 16px;
    color: #686868;
    margin-left: 5px;
    font-weight: 500;
  }
  .links {
    font-size: 1em;
    color: #212121;
  }
  .send-button-burger {
    display: block;
    margin-top: 30px;
  }
  .phone-button-burger {
    text-decoration: none;
    margin-left: 30px;
  }
  .button-burger {
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: #0a2c87;
    height: 50px;
    width: 10em;
    border-radius: 50px;
    box-sizing: border-box;
    padding: 10px 30px;
    color: white;
    font-size: 1em;
  }
  .button-burger > img {
    width: 20px;
    margin-right: 10px;
  }
  #phone-burger {
    background-color: #00ad3a;
  }
  #phone-burger:hover {
    background-color: #00c43c;
  }
@media only screen and (max-width : 780px) {
  .bm-burger-button {
    top: 30px;
    right: 42px;
  }
}
</style>