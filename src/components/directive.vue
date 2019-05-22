<template>
    <!--自定义指令：全局要在main.js中配置-->
  <div>
    <!--v-focus:当进入页面的时候选择中输入框-->
    <input type="text" v-focus>
    <!--v-asd:加载之后添加样式-->
    <p v-asd>666</p>
  </div>
</template>

<script>
    export default {
        name: "directive",
      //自定义指令----局部的写法
      directives: {
        focus: {
          // 指令的定义
          inserted: function (el) {
            el.focus()
          }
        },
        asd:{
          inserted: function (el) {
            el.style.color = "red"
          }
        }
      }
    }
</script>

<style scoped>

</style>
