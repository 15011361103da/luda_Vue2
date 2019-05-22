<template>
    <!--过滤器：filters-->
  <div>
    <p>{{price | price11}}</p>
  </div>
</template>

<script>
    export default {
        name: "filters",
      data(){
          return{
            price:20
          }
      },
      filters:{
          price11(value){
            if(typeof value === 'number'){
              return "￥" + value;
            }
            return value;
          }
      }
    }
</script>

<style scoped>

</style>
