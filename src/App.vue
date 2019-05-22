<template>
  <div id="app">
    <img src="./assets/logo.png">
    <filters/>
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
import parent from './components/slots/parent'
import big from './components/comkeep/big'
import anim from './components/anim/anim'
import directive from './components/directive'
import filters from './components/filters'

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
    father1,
    parent,
    big,
    anim,
    directive,
    filters
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
