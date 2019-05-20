<template>
    <div>
      <button @click="showHide">显示/隐藏</button>
      <transition name="fade">
        <p v-show="show">显示/隐藏</p>
      </transition>

    </div>
</template>

<script>
    export default {
      name: "anim",
      data(){
        return{
          show:true
        }
      },
      methods:{
        showHide(){
          this.show = !this.show;
        }
      },
    }
</script>

<style scoped>
  /*.fade-enter-active,.fade-leave-active{
    transition: opacity 2s;
  }
  .fade-enter,.fade-leave-to{
    opacity: 0;
  }*/
/**
  显示：opacity：0-1；
  隐藏：opacity：1-0；
*/
  .fade-enter,.fade-leave-to{ /*entter：开始*/
    /*opacity: 0;*/
    transform: translate(0,-100px);
  }
  .fade-enter-active,.fade-leave-active{  /*过程*/
    /*transition: 2s;*/
    transition: all 2s;
  }
  .fade-enter-to,.fade-leave{  /*结束*/
    /*opacity: 1;*/
    transform: translate(-10px,0);
  }
</style>
