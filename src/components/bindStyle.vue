<template>
    <div>
      <p v-bind:class="{active:isActive}">6666</p>
      <p v-bind:class="styleObj">6666</p>
      <p v-bind:class="[demo1,demo2]">777</p>
      <ul>
        <li :class="[{active:index%2 == 1},'indo'+index]" v-for="(name,index) in names">{{name}}</li>
      </ul>
      <input type="text" v-model="mes">
      <p>{{mesage}}</p>
      <p>{{mesage}}</p>
      <p>{{mesage}}</p>
      <p>{{mesage}}</p>
      <p>{{mesage}}</p>
      <p>{{mesage}}</p>
      <button class="btn" v-on:click="add">测试计算属性缓存</button>
    </div>
</template>

<script>
    export default {
      name: "bindStyle",
      data(){
        return {
          //测试v-bind
          isActive:true,
          isDeom:true,
          //监听v-model绑定的数据
          mes:'666',
          num:1,
          demo1:"demo11",
          demo2:"demo22",
          names:[
            "luda","xiuyuchuan","ajgffnmcdcc"
          ]
        }
      },
      //方法
      methods:{
        add(){
          this.num += 10;
        },
      },
      /*计算属性:在HTML DOM加载完后执行，具有缓存的功能，也就是如果计算的数据没发生变化，会使用缓存中的数据，不会再次计算*/
      computed:{
        mesage(){   //方法的名字与变量的名字相同
          console.log(this.num);
          return this.num;
        },
        styleObj(){
          return {
            active:this.isActive,
            deom:this.isDeom
          };
        }
      },
      /*监听：实时监听v-model的数据；变量的名字要与方法名相同*/
      watch:{
        mes(){
          console.log(this.mes);
        },
      }
    }
</script>

<style>
  .active{
    color:red;
  }
  .btn{
    border-radius:10px;
    width:630px;
    height:90px;
    background:linear-gradient(90deg,rgba(81,80,204,1) 0%,rgba(102,100,255,1) 52%,rgba(132,131,255,1) 100%);
  }
</style>
