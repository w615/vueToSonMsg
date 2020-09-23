<template>
  <div class="son">
    <h3>我是子组件</h3>
    <ul>
      <li v-for="(item,index) in toSon"  :key="index">{{item}}</li>
    </ul>
  </div>
</template>
<script>
export default {
  props:{
    toSon:Array
  },
}
</script>

<style>
.son{
  background: #ff0;
  padding:20px;
  border:10px solid red;
}

</style>