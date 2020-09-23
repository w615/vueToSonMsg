<template>
  <div id="app">
    <One v-on:AddHandle="AddIptVal"></One>
    <!--one通过$emit 触发监听到的值传给app    从 app--two  是父组件通过props对子组件通讯-->
    <Two :dataIpt="list"></Two>
  </div>
</template>
<script>
// 引入one 和two
import One from './components/one'
import Two from './components/two'
export default {
  data(){
    return {
      list:[]
    }
  },
  components:{
    One,
    Two
  },
  methods:{
    AddIptVal(iptVal){
      this.list.push(iptVal)

    }
  }
}
</script>

<style>

</style>