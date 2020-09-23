<template>
<!--  父组件通过props向子组件传值 -->
<div class="father">
  <h1>我是父组件</h1>
  <input type="text" v-model="value">
  <button @click="AddAction">提交到子组件</button>
   <!-- 子组件获取list  通过v-bind绑定toSon -->
  <Son :toSon="list"/>
</div>
</template>
<script>
//引入子组件
import Son  from './son'
export default {
  data(){
    return{
      list:[],
      value:''
    }
  },
  components:{
    Son
  },
  methods:{
    AddAction(value){
      console.log(this.value);
      this.list.push(this.value)
      console.log();
      this.value=""
      console.log(this.list);
    }
  }
}
</script>

<style>
.father{
  padding:50px;
  background: skyblue;
  border:5px solid #ace
}

</style>