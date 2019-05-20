<template>
    <div>
      父组件
      <child>
        <!--插槽：
        单个插槽，
        具名插槽（传递多个插槽时，可以使用）
        作用域插槽:子给父传递数据
        -->
        <p class="ptest" slot="name1">我是插槽1</p>
        <p class="ptest" slot="name2" slot-scope="props">{{props.text}}</p>
      </child>
    </div>
</template>

<script>
  import child from './child'
    export default {
      name: "parent",
      data(){
        return{

        }
      },
      components:{
        child
      },
    }
</script>

<style scoped>

</style>
