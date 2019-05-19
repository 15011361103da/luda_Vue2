<template>
    <div class="">
      <!--监听事件v-model绑定的数据的变化：mes变量与watch的方法名字相同-->
      <input v-model="mes"></input><br/>
      {{mes}}
    </div>
</template>

<script>
    export default {
      name: "formdata",
      data(){
        return{
          mes:''
        }
      },
      watch:{
        mes(data){
          console.log(data)
        }
      }

    }
</script>

<style>

</style>
