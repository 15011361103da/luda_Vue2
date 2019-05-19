<template>
    <div>
      父组件
      <input type="text" v-model="num">
      <son @sendMes="getMes" :num="getNum"/>
      {{mes}}
    </div>
</template>

<script>
  import son from './fatherSon1'
    export default {
      name: "father1",
      data(){
        return{
          mes:'',
          num:5
        }
      },
      components:{
        son
      },
      /*计算属性：当数据发生变化了需要重新计算
      * 此处是用来转换input的数据类型，将String转换为Number*/
      computed:{
        getNum(){
          return this.num -0;
        }
      },
      methods:{
        getMes(data){
          this.mes = data;
        }
      },
    }
</script>

<style>

</style>
