<template>
  <div id="app">
    
    <WithDrawMoney msg="Welcome to Your Vue.js App"/>
    <!-- <WithDrawMoney msg="Welcome to Your Vue.js App"/> -->
  </div>
</template>

<script>
import WithDrawMoney from './components/WithDrawMoney.vue'


export default {
  name: 'App',
  components: {
    // Recharge,WithDrawMoney
    WithDrawMoney
  }
}
</script>

<style lang="scss" scoped>
@import "./styles/color.scss";
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
