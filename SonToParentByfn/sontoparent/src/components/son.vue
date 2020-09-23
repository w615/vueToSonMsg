<template>
  <div class="son">
    <h1>展示子组件</h1>
    <ul>
      <li v-for="(item,index) in city" :key="index">
        {{item}}
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  props:{
    // 接收父组件传来的值
    //把接收的数值放到数组里面
    city:{
      type:Array,
      required:true,
    },
  list:[]
  },
}
</script>

<style>
  .son{
    background: #ccc;
    padding:50px;
  }
</style>