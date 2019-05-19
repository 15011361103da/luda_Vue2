<template>
    <div class="event">
      <ul>
        <li v-on:click="getName(name,index,$event)" v-for="(name,index) in names">{{name}}</li>
      </ul>
      <input type="text" v-on:keyup.enter="getkeyupInfo">
    </div>
</template>

<script>
    export default {
      name: "Event",
      data(){
        return{
          names:[
            'luda',
            'xiuyuychuan',
            'lujianzhong'
          ]
        }
      },
      methods:{
        getName(data,index,event){
          console.log(data)
          this.names.splice(index,1);
          console.log(event)
        },
        getkeyupInfo(event){
          console.log(event);
        }
      }
    }
</script>

<style>

</style>
