<template>
  <div class="dashboard">
    <div class="item1"></div>
    <div class="item2"></div>
    <div class="item3"></div>
    <div class="item4"></div>
    <div class="item1"></div>
    <div class="item2"></div>
    <FlexItem/>
    <div class="item3"></div>
    <FlexItem/>
    <div class="item4"></div>
    <div style="
      background-color: #325496;
      flex-grow: 10;
      width: 100px;
      min-height: 100px;
    "></div>
    <div style="
      background-color: #5d729a;
      flex-grow: 5;
      width: 100px;
      min-height: 200px;
    "></div>
    <FlexItem/>
  </div>
</template>

<script>
import FlexItem from './FlexItem';

export default {
  name: 'hello',
  components: {
    FlexItem
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.dashboard {
  display: flex;
  flex-flow: row wrap;
  justify-content: space-between;
  align-items: stretch;
  width: 100%;
  height: 100%;
}
.item1 {
  background-color: #325496;
  flex-grow: 1;
  width: 100px;
  min-height: 100px;
}
.item2 {
  background-color: #5a92e7;
  flex-grow: 2;
  width: 200px;
  min-height: 100px;
}
.item3 {
  background-color: #238ade;
  flex-grow: 3;
  width: 100px;
  min-height: 100px;
}
.item4 {
  background-color: #14687e;
  flex-grow: 4;
  width: 200px;
  min-height: 100px;
}


</style>
