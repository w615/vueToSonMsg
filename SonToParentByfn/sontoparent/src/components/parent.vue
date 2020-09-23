<template>
<div class="parent">
  <h1>父组件</h1>
  <h2>当前的城市为：{{selectCity}}</h2>
                   <!--满足 selectCity == item  执行class 这个绑定的属性 -->
  <button v-for="item in cities" :key="item" :class="{active: selectCity == item }"
  @click=" SelectCity(item)">
    {{item}}
  </button>
  <!-- 父组件通过props向子组件传值  子元素接收：city-->
  <Son :city="cities"></Son>
  <!-- 子组件上绑定的属性为函数 子元素用props 接收次函数之后可以调用-->
  <Add :callback="AddHandle" ></Add>
</div> 
</template>
<script>
// 引入子组件
import Son from './son'
import Add from './add'
export default {
  data(){
    return {
      // 当前的城市
      selectCity:'',
      cities:['郑州','驻马店']
    }
  },
  components:{
    Son,
    Add
  },
  // 方法
  methods:{
    SelectCity(item){
      this.selectCity = item
    },
    // 这个函数通过props传入到子组件中，被调用了 传入的实参为this.value  
    AddHandle(city){
      this.cities.push(city)
    }
  }

}
</script>

<style>
.parent{
  border:2px solid #aaee;
  padding:50px;

}
.active{
  background:lime;
}

</style>