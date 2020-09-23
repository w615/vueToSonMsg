<template>
<div class="one">
  <h2>我是one组件</h2>
  <!-- 点击1组件上的提交把 input上的值传递给 父组件 -->
  <input type="text" v-model="iptVal" >
  <button @click="AddAction">提交</button>
</div>
  
</template>

<script>
// one通过App共有的父组件中介作用传递值给two
export default {
  data(){
    return {
      iptVal:'',
    }
  },
  methods:{
    AddAction(){
      this.$emit('AddHandle',this.iptVal)
      this.iptVal=''
    }
  }

}
</script>

<style>
.one{
  padding:20px;
  background: #999;
}
</style>