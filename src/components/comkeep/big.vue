<template>
  <div>
    <!--动态绑定组件-->
    big
    <keep-alive>  //缓存组件
      <component :is="currentvView"></component>
    </keep-alive>

    <button @click="changeView">切换组件</button>
  </div>
</template>

<script>
  import small1 from './small1'
  import small2 from './small2'
    export default {
      name: "big",
      data(){
        return{
          currentvView:"small1",
          flag:true
        }
      },
      components:{
        small1,
        small2
      },
      methods:{
        changeView(){
          if(this.flag){
            this.currentvView = 'small2';
            this.flag = false;
          }else{
            this.currentvView = 'small1'
            this.flag = true;
          }

        }
      }

    }
</script>

<style scoped>

</style>
