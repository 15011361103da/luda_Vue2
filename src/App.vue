<template>
  <div id="app">
    <img src="./assets/logo.png">
    <father1/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import Event from './components/Event'
import formdata from './components/formdata'
import vuelife from './components/vue-life'
import Styles from './components/bindStyle'
import vforKey from './components/v-for-key'
import father from './components/father'
import father1 from './components/father1'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Event,
    formdata,
    vuelife,
    Styles,
    vforKey,
    father,
    father1
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
