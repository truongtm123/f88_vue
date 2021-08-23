<template>
  <div id="app">
    
    <ReportTransaction msg="Welcome to Your Vue.js App"/>
    <!-- <WithDrawMoney msg="Welcome to Your Vue.js App"/> -->
  </div>
</template>

<script>
import ReportTransaction from './components/ReportTransaction.vue'


export default {
  name: 'App',
  components: {
    // Recharge,WithDrawMoney
    ReportTransaction
  }
}
</script>

<style lang="scss">
@import "./styles/color.scss";
@import "../src/styles/common.scss";
#app{
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  padding: 20px 20px 0 20px;
  background-color: $reset-border-color;
  display: block;
  overflow: hidden;
}
</style>
