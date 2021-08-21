<template>
  <div id="app">
    
    <Recharge msg="Welcome to Your Vue.js App"/>
    <!-- <WithDrawMoney msg="Welcome to Your Vue.js App"/> -->
  </div>
</template>

<script>
import Recharge from './components/Recharge.vue'


export default {
  name: 'App',
  components: {
    // Recharge,WithDrawMoney
    Recharge
  }
}
</script>

<style>
#app{
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  padding: 20px 20px 0 20px;
  background-color: #f6f9fb;
  display: block;
  overflow: hidden;
}
</style>
