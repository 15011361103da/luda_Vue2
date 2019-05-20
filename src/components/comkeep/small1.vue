<template>
  <div>
    {{mes}}
    <button @click="changeMes">测试是否重新渲染</button>
  </div>
</template>

<script>
    export default {
      name: "small1",
      data(){
        return{
          mes:'small1'
        }
      },
      methods:{
        changeMes(){
          this.mes = 'small11111111'
        }
      }
    }
</script>

<style scoped>

</style>
