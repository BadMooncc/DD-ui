<style lang="scss">
  @import "../assets/scss/index";
  .header {
    background-color: #fff;
    box-shadow: 0 10px 60px 0 rgba(29,29,31,0.07);
    opacity: 0.98;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 80px;
    transition: all .3s;
    z-index: 100;
    .header-container{
      width: 90%;
      margin: 0 auto;
      display: flex;
      align-items: center;
      height: 80px;
      justify-content: space-between;
    }
  }
</style>
<template>
  <header class="header" :style="$route.name === 'index' ? 'box-shadow:none' : 'box-shadow:0 2px 3px 0 rgba(29,29,31,0.07)'">
    <div class="header-container">
      <router-link :to="{name: 'index'}"><img src="/static/images/logo.png" width="100"></router-link>
      <!-- <router-link :to="{name: 'giud'}">组件</router-link> -->
      <!-- <button @click="handle">组件</button> -->
    </div>
  </header>
</template>

<script>
  export default {
    data () {
      return {}
    },
    methods: {
      handle() {
        window.open('http://localhost:8080/#/','_self')
      }
    }
  }
</script>
