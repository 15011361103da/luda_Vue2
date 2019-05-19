<template>
  <!--vue基本指令-->
  <div class="hello">
    <p>{{hello}}</p>

    <!--  v-html与v-text区别：v-html会解析变量里面的标签；v-text不会解析，直接将标签显示成文本 -->
    <p v-html="html"></p>
    <p v-text="html"></p>

    <!--v-bind：以动态地切换class-->
    <p v-bind:class="cla">动态绑定class</p>
    <p v-bind:title="tit">v-bind可以动态绑定任何属性，不仅是class</p>
    <p>{{message.split("").reverse().join("")}}</p>

    <!--v-if:懒加载，当第一次为true的时候才会加载，切换开销大，
      v-show：不管第一次为true还是false，都会加载，只是切换display
    -->
    <div v-if="vif">v-if显示</div>

    <!---->
    <button v-on:click="add">监听事件:v-on:click</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      hello:'hello Vue',
      html:'<span>sdfs</span>',
      cla:'bin',
      tit:'动态绑定titlt属性成功了',
      message:'hello',
      vif:true,

    }
  },
  methods:{
    add(){
      alert("监听事件成功");
      this.vif = !this.vif;
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.bin{
  color: red;
}
</style>
