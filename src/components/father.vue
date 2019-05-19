<template>
    <div>
      <!--父组件向子组件传值-->
      父亲
      <!--v-bind绑定动态的数据，向子组件传递数据-->
      <son :title="mes" :life="lifeMes" :num="num" />
      <!--测试改变数据是否可以传递到子组件-->
      <button @click="changeMes">改变需要传递的数据</button>
      <!--测试v-model传递到子组件的数据-->
      <input type="text" v-model="lifeMes">
    </div>
</template>

<script>
  import son from './fatherSon'
    export default {
      name: "father",
      data(){
        return{
          mes:'这里是父组件的数据传递到子组件',
          lifeMes:'',
          num:6,
          myobj:{
            name:"ienw",
            age:10
          }
        }
      },
      components:{
        son
      },
      methods:{
        changeMes(){
          this.mes = '我是修改之后的数据';
        },
      },
    }
</script>

<style>

</style>
