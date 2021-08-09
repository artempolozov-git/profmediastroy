<template>
  <div id="app">
    <router-view name="header"></router-view>
    <div id="app-content">
      <transition name="app-router-fade" mode="out-in">
        <router-view :key="defaultViewKey"></router-view>
      </transition>
    </div>
    <router-view name="footer"></router-view>
  </div>
</template>

<script>
    export default {
        name: 'App',
        components: {

        },
        computed: {
            defaultViewKey: function() {
                return this.$route.name;
            }
        }
    }
</script>

<style>
  html, body {
    height: 100%;
  }
  body {
    margin: initial;
    font-family: PMS;
    font-size: 16px;
    font-weight: 500;
  }
  #app {
    display: flex;
    flex-direction: column;
    min-height: 100%;
    background-color: white;
  }
  @font-face {
    font-family: PMS;
    src: url('./assets/PMS-Bold.ttf');
    font-weight: bold;
  }
  @font-face {
    font-family: PMS;
    src: url('./assets/PMS-Medium.ttf');
    font-weight: normal;
  }
  @font-face {
    font-family: PMS;
    src: url('./assets/PMS-Regular.ttf');
    font-weight: 500;
  }
  #app-content {
    flex: 1 0 auto;
    max-width: 1920px;
    align-self: center;
    width: -webkit-fill-available;
  }
</style>
