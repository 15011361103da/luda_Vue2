<template>
    <div class="vforKey">
      <!--
      测试v-for的key的作用：
        vue中列表循环需加:key="唯一标识" 唯一标识可以是item里面id index等，因为vue组件高度复用增加Key可以标识组件的唯一性，
        为了更好地区别各个组件 key的作用主要是为了高效的更新虚拟DOM
      -->
      <ul>
        <li v-for="item in names">
          <input type="checkbox">
          {{item.id}}---{{item.name}}
        </li>
      </ul>
      <label>
        ID:
        <input type="text" v-model="id">
      </label><br/>
      <label>
        Name:
        <input type="text" v-model="name">
      </label><br/>
      <button v-on:click="addList">改变数组</button>
    </div>
</template>

<script>
    export default {
      name: "v-for-key",
      data(){
        return{
          names:[
            {
              id:1,
              name:'郑恺'
            },
            {
              id:2,
              name:'安卓拉北鼻'
            },
            {
              id:3,
              name:'朱亚文'
            },
          ],
          id:'',
          name:'',
        }
      },
      methods:{
        addList(){
          this.names.unshift({id:this.id,name:this.name});
        },
      },

    }
</script>

<style>
  li{
    list-style: none;
  }
</style>
