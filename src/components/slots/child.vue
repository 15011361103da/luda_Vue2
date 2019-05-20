<template>
    <div>
      子组件
      <!--插槽-->
      <slot name="name1">666<!--此处如果没有将插槽传递过来，则显示这里默认的数据--></slot>
      <hr/>
      <slot name="name2" text="jkh">888</slot>
    </div>
</template>

<script>
    export default {
      name: "child",
      data(){
        return {

        }
      },

    }
</script>

<style scoped>
  .ptest{
    color:red;
  }
</style>
