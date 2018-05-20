<template>
  <div>
    <p>我是商品列表页面</p>
    <p>商品id:{{$route.params.goodsId}}</p>
    <p>用户id:{{$route.params.userId}}</p>
    <router-link to="/goods/head">显示商品标题</router-link>
    <router-link to="/goods/image">显示商品图片</router-link>
    <div>
      <router-view/>
    </div>
    <router-link to="/cart">link跳转至购物车界面</router-link>
    <button @click="jump">按钮跳转至购物车界面</button>
    <button @click="jumpWithParam">按钮跳转至购物车界面</button>
  </div>
</template>

<script>
  export default {
    name: "goods-list",
    methods: {
      jump() {
        this.$router.push("/cart")
      },
      jumpWithParam() {
        this.$router.push("/cart?cartId=13")
      }
    }
  }
</script>

<style scoped>

</style>
