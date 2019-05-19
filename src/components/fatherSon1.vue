<template>
    <div>
      子组件
      <button @click="sendMes">子传父</button>
    </div>
</template>

<script>
    export default {
      name: "fatherSon1",
      data(){
        return{
          mes:'我是子组件传递的数据',
        }
      },
      props:{
        num:{
          type:Number,
          default:5
        }
      },
      computed:{
        addMes(){
          return this.num *5;
        }
      },
      methods:{
        //子组件传递数据到父组件，
        sendMes(event){
          //参数：第一个是key，作用是在父组件根据此key查找到传输的数据；第二个参数是数据；
          this.$emit("sendMes",this.addMes)
        }
      }
    }
</script>

<style>

</style>
