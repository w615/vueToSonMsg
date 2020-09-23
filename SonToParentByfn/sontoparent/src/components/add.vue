<template>
  <div class="add">
    <h1>添加子组件</h1>
    <input type="text" v-model="value">
    <button @click="AddAction">添加</button>
  </div>
</template>
<script>
export default {
  props:{
    // 子组件接收到这个函数之后就可以调用
    callback:Function,
  },
  data(){
    return{
      value:'',
    }
  },
  methods:{
 // 触发添加按钮的时候调用传过来的回调函数，把this.value 传入这个回调函数 达到向父元素传值的效果
    AddAction(){
      this.callback(this.value)
      this.value=''
    }
  }
}
</script>

<style>
.add{
  background: skyblue;
  padding:20px;
}
</style>