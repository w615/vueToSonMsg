<template>
  <div id="app">
    <father></father>
  </div>
</template>

<script>
// 引入父组件
import father from './components/father'
import Son from './components/son'
 // 向外暴露father
  export default {
    components:{
      father,
      Son
    }

  
}
</script>
<style>
html,body{
  width:100%;
  height:100%；
}

</style>
<style>
html,body{
  background: skyblue;
}
</style>
