<template>
  <!--
  enter/enter-active/enter-to
  leave/leave-active/leave-to
  动画库：<link href="https://cdn.jsdelivr.net/npm/animate.css@3.5.1" rel="stylesheet" type="text/css">
  在index.html中引入


  -->
    <div>
      <button @click="showHide">过渡</button>
      <transition name="fade">
        <p v-show="show">显示/过渡</p>
      </transition>

      <button @click="showHideAnim">动画</button>
      <transition name="hello">
        <p v-show="showAnim">动画</p>
      </transition>

      <button @click="animLibs">第三方</button>
      <transition name="world" enter-active-class="animated flip"
                  leave-active-class="animated flip">
        <p v-show="showAnimLibs">
          第三方动画
        </p>
      </transition>

    </div>
</template>

<script>
    export default {
      name: "anim",
      data(){
        return{
          show:true,  //过度
          showAnim:true,  //动画
          showAnimLibs:true  //第三方动画库
        }
      },
      methods:{
        showHide(){
          this.show = !this.show;
        },
        showHideAnim(){
          this.showAnim = !this.showAnim;
        },
        animLibs(){
          this.showAnimLibs = !this.showAnimLibs;
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

  .hello-enter-active{
    animation:bounce-in 1s ease;
  }
  .hello-leave-active{
    animation:bounce-out 1s ease;
  }

  @keyframes bounce-in {
    0% {
      transform: scale(0);
    }
    50% {
      transform: scale(1.5);
    }
    100% {
      transform: scale(1);
    }
  }
  @keyframes bounce-out {
    0% {
      transform: scale(1);
    }
    50% {
      transform: scale(1.5);
    }
    100% {
      transform: scale(0);
    }
  }
</style>
