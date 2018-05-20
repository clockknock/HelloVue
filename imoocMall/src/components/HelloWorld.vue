<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <!-- v-on:后面的名称是给component中的$emit绑定回调用的 -->
    <Counter v-bind:num="num" v-on:incre="increment" v-on:decre="decrement"/>
    <p>parentNum:{{num}}</p>
  </div>
</template>

<script>
  import Counter from './Counter'

  export default {
    name: 'HelloWorld',
    data() {
      return {
        num:10,
        msg: 'Welcome to Your Vue.js App'
      }
    },
    components: {
      Counter
    },
    methods:{
      increment(){
        this.num++
      },
      decrement(){
        this.num--
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
