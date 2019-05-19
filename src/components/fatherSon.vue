<template>
    <div>
      儿子:{{title}}
      {{life}}<br/>
      {{num * 2}}<br/>
      {{objdata.name}}
    </div>
</template>

<script>
    export default {
      name: "fatherSon",
      data(){
        return{

        }
      },
      //普通书写方式和
    /*props:[
      "title",
      "life"
    ]*/
    //指定数据类型
      props:{
        title:String,
        life:{
          type:String, //传递的数据类型
          required:false //是否是必传项
        },
        num:{
          type:Number,
          default:5,  //默认值
          required:false
        },
        objdata:{
          type:Object,
          //如果传递的是对象，需要用function
          default: function () {
            return{
              name:'未知',
              age:666
            }
          }
        }
      }
    }
</script>

<style>

</style>
