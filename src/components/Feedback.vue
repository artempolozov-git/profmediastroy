<template>
  <div id="feedback" style="display: none;">

    <div class="overlay">
      <form id="feedback-form" action="" method="POST" class="form-wrapper">

        <div style="display: block; width: 100%;">
          <div class="title-form">Заказ продукции</div>
          <div class="button-close">
            <span style="font-family: 'Gilroy'" class="closebtn" @click="feedbackForm">&times;</span>
          </div>

          <div class="select-name">
            <div>
              <div class="input-title">
                <span>Введите имя:</span>
              </div>
              <div class="form-group">
                <input name="Имя" type="text" class="input-text" placeholder="Имя" required>
              </div>
            </div>
          </div>

          <div class="select-name">
            <div>
              <div class="input-title">
                <span>Номер телефона:</span>
              </div>
              <div class="form-group">
                <masked-input v-model="phone" mask="\+\7 (111) 111 11-11" name="Телефон" type="text" class="input-text" placeholder="Телефон" required />
              </div>
            </div>
          </div>

          <div class="select-name">
            <div>
              <div class="input-title">
                <span>Введите email:</span>
              </div>
              <div class="form-group">
                <input name="Email" type="text" class="input-text" placeholder="Email" required>
              </div>
            </div>
          </div>

          <div class="select-input">
            <div>
              <div class="input-title">
                <span>Выберите услугу:</span>
              </div>
              <div class="form-group">
                <select name="Услуга" class="input-form">
                  <option value="Наружная реклама">Изготовление наружной рекламы</option>
                  <option value="Аренда и продажа стендов">Аренда и продажа стендов</option>
                  <option value="Бизнес-полиграфия">Производство бизнес-полиграфии</option>
                </select>
              </div>
            </div>
          </div>

          <div class="form-group-comment">
            <div class="input-title">
              <span>Комментарий:</span>
            </div>
            <textarea name="Комментарий" class="form-comment" placeholder="Введите дополнительную информацию по заказу"></textarea>
          </div>
          <div class="button-container">
            <input type="submit" id="form-button" class="feedback-button" value="Заказать">
            <span class="form-status" id="form-status"></span>
          </div>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
    import MaskedInput from 'vue-masked-input'
    export default {
        components: {
            MaskedInput
        },
        data() {
            return {};
        },
        computed: {

        },
        methods: {
            feedbackForm(){
                var form = document.getElementById("feedback");
                form.style.display = (form.style.display == 'none') ? 'block' : 'none'
            }
        },
        mounted() {

            // get the form elements defined in your form HTML above

            var form = document.getElementById("feedback-form");
            var button = document.getElementById("form-button");
            var status = document.getElementById("form-status");

            // Success and Error functions for after the form is submitted

            function success() {
                form.reset();
                button.style = "display: none ";
                status.innerHTML = "Спасибо, мы скоро c Вами свяжемся!";
            }

            function error() {
                status.innerHTML = "Произошла ошибка при отправке!";
            }

            // handle the form submission event
            console.log(form);
            form.addEventListener("submit", function(ev) {
                ev.preventDefault();
                var data = new FormData(form);
                ajax(form.method, form.action, data, success, error);
            });


            // helper function for sending an AJAX request

            function ajax(method, url, data, success, error) {
                var xhr = new XMLHttpRequest();
                xhr.open(method, url);
                xhr.setRequestHeader("Accept", "application/json");
                xhr.onreadystatechange = function() {
                    if (xhr.readyState !== XMLHttpRequest.DONE) return;
                    if (xhr.status === 200) {
                        success(xhr.response, xhr.responseType);
                    } else {
                        error(xhr.status, xhr.response, xhr.responseType);
                    }
                };
                xhr.send(data);
            }
        }
    };
</script>

<style scoped>
  .button-close {
    transition: 0.3s;
    position: absolute;
    z-index: 100;
    right: 35px;
    top: 20px;
  }
  .closebtn {
    color: #212121;
    font-weight: normal;
    font-size: 5em;
    line-height: 1em;
    cursor: pointer;
  }
  .closebtn:hover {
    color: #4c4c4c;
  }
  .closebtn::selection {
    outline: none;
    background: transparent;
  }
  #feedback {
    height: 100%;
    width: 100%;
    position: fixed;
    background-color: rgba(33, 33, 33, 0.71);
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    z-index: 100;
  }
  .overlay {
    height: 100%;
    width: 50em;
    top: 3em;
    right: 0;
    bottom: 0;
    left: 0;
    margin: auto;
    overflow: auto;
    z-index: 100;
    position: fixed;
  }
  .form-wrapper {
    display: flex;
    padding: 80px 120px;
    box-sizing: border-box;
    background-color: white;
  }
  .title-form {
    font-size: 2.5em;
    font-weight: bold;
    color: #212121;
    margin-bottom: 1em;
  }
  .select-name {
    display: flex;
    margin-bottom: 1.5em;
  }
  .select-input {
    display: flex;
    align-items: center;
    margin-bottom: 1.5em;
  }
  .input-title {
    display: flex;
    margin-bottom: 1em;
  }
  .input-title > span {
    color: #212121;
    font-size: 1.5em;
    font-weight: bold;
  }
  .form-group {
    display: flex;
    align-items: center;
  }
  .input-form {
    width: 26.5em;
    font-family: PMS;
    color: #4c4c4c;
    font-weight: 500;
    font-size: 1.3em;
    padding: 15px;
    outline: none;
    border: 2px solid #dfdfe2;
  }
  .input-form:focus {
    border: 2px solid #0a34af;
  }
  .input-text {
    width: 25em;
    font-family: PMS;
    color: #4c4c4c;
    font-weight: 500;
    font-size: 1.3em;
    padding: 15px;
    outline: none;
  }
  .input-text {
    border: 2px solid #dfdfe2;
  }
  .input-text:focus {
    outline: none;
    border: 2px solid #0a34af;
  }
  .form-comment {
    width: 25em;
    height: 129px;
    font-family: PMS;
    font-weight: 500;
    color: #4c4c4c;
    font-size: 1.3em;
    padding: 15px;
    outline: none;
    border: 2px solid #dfdfe2;
    resize: none;
  }
  .form-comment:focus {
    border: 2px solid #0a34af;
  }
  .button-container {
    display: flex;
    justify-content: center;
  }
  .feedback-button {
    width: 10em;
    height: 3.5em;
    margin-top: 30px;
    text-align: center;
    color: white;
    font-size: 1.5em;
    font-family: PMS;
    font-weight: normal;
    background-color: #0a2c87;
    border: none;
  }
  .feedback-button:hover {
    cursor: pointer;
    background-color: #132453;
  }
  .feedback-button::selection {
    outline: none;
    background: transparent;
  }
  .feedback-button:focus {
    outline: none;
  }
  .form-status{
    margin-top: 30px;
    text-align: center;
    font-family: PMS;
    font-weight: normal;
    font-size: 1.3em;
    color: #00ad3a;
  }
  .overlay::-webkit-scrollbar {
    display: none; /* Safari and Chrome */
  }
  @media only screen and (max-width : 1680px) {
    .overlay {
      top: 5em;
    }
  }
  @media only screen and (max-width : 1536px) {
    .overlay {
      top: 3em;
    }
  }
  @media only screen and (max-width : 800px) {
    .overlay {
      top: 10em;
    }
  }
  @media only screen and (max-width : 600px) {
    .overlay {
      width: 100vw;
      top: 0;
    }
    .form-wrapper{
      width: 100%;
      height: 100vh;
      align-items: center;
    }
    .input-form {
      background-color: white;
    }
    .input-date {
      background-color: white;
    }
  }
  @media only screen and (max-width : 360px) {
    .input-text {
      font-size: .8em;
    }
    .input-title > span {
      font-size: 1em;
    }
    .feedback-button {
      font-size: 1em;
    }
  }
</style>