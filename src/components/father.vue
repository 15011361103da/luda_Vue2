<template>
    <div>
      父亲
      <son/>
    </div>
</template>

<script>
  import son from './fatherSon'
    export default {
      name: "father",
      data(){
        return{

        }
      },
      components:{
        son
      }
    }
</script>

<style>

</style>
