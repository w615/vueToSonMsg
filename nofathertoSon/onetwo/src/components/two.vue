<template>
  <div class="two">
    <h3>我是two组件</h3>
    <ul>
      <li v-for="(item ,index) in dataIpt" :key="index">
        {{item}}
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  props:{
    dataIpt:Array
  }
}
</script>

<style>
.two{
  padding:20px;
  background: #aec;
}
</style>