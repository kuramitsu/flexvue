<template>
  <div id="app">
    <header>
      <div>FlexVue</div>
    </header>
    <main>
      <flex></flex>
    </main>
    <footer>
      <div>&copy; kuramitsu</div>
    </footer>
  </div>
</template>

<script>
import Hello from './components/Hello';
import Flex from './components/Flex';

export default {
  name: 'app',
  components: {
    Hello,
    Flex
  }
}
</script>

<style>
html, body, #app {
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
}
#app {
  display: flex;
  flex-flow: column nowrap;
  justify-content: flex-start;
  align-items: flex-start;
}
header {
  width: 100%;
  height: 40px;
  background-color:#444;
  color: #CCC;
  flex-shrink: 0;
  display: flex;
  flex-flow: row nowrap;
  justify-content: flex-start;
  align-items: center;
}
header>div {
  margin: 10px;
}
main {
  height: calc(100% - 70px);
  width: 100%;
  overflow: auto;
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
  align-items: center;
}
footer {
  width: 100%;
  height: 30px;
  background-color:#444;
  color: #CCC;
  flex-shrink: 0;
  display: flex;
  flex-flow: row nowrap;
  justify-content: center;
  align-items: center;
}




/*
header {
  position: fixed;
  padding: 0px 10px;
  top: 0px;
  left: 0px;
  width: 100%;
  height: 40px;
  background-color:#444;
  color: #CCC;
  display: flex;
  flex-flow: row nowrap;
  justify-content: flex-start;
  align-items: center;
}
main {
  overflow: auto;
  margin: 0;
  padding-top: 40px;
  padding-bottom: 30px;
  height: calc(100% - 70px);
  width: 100%;
  min-height: 200px;
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
  align-items: center;
}
footer {
  position: fixed;
  bottom: 0px;
  left: 0px;
  width: 100%;
  height: 30px;
  background-color:#444;
  color: #CCC;
  display: flex;
  flex-flow: row nowrap;
  justify-content: center;
  align-items: center;
}
*/
</style>
