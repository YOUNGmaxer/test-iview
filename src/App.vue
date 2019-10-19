<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <br/>
    <Button @click="isAlertOn = true">打开弹窗</Button>
    <my-alert
      :isAlertOn="isAlertOn"
      @modalStatusChange="updateAlertOn"
    ></my-alert>
  </div>
</template>

<script>
import MyAlert from './components/MyAlert';

export default {
  name: 'app',
  components: {
    MyAlert
  },
  data() {
    return {
      isAlertOn: false
    }
  },
  methods: {
    updateAlertOn(curStatus) {
      this.isAlertOn = curStatus;
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
