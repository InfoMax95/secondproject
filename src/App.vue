<template>
  <div id="app">
    <h1 class="text-white">ciaociacoaico</h1>
    <MyHeader/>
    <MyMain/>
    <MyFooter/>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue';
import MyMain from './components/MyMain.vue';
import MyFooter from './components/MyFooter.vue';

export default{
  name: 'App',
  components: {
    MyHeader,
    MyMain,
    MyFooter
  }
}
</script>


<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  // text-align: center;
  // color: #2c3e50;
}
</style>
