<template>
  <div id="app">
   <Parent></Parent>

  </div>
</template>

<script>
// 移入其他的组件
import Parent from './components/parent'
export default {
  components:{
    Parent
  }

}
</script>

<style>
#app{
  background: lightslategrey;
}

</style>