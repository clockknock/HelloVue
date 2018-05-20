<template>
  <div>
    <button @click="increment">+</button>
    <button @click="decrement">-</button>
    <p>{{count}}</p>

  </div>
</template>

<script>
  export default {
    name: "counter",
    props:["count"],
    data() {
      return {
        msg: 'hello vue',
        count: 0
      }
    },
    methods: {
      increment() {
        this.$emit("incre")
      },
      decrement() {
        this.$emit("decre")
      }
    }

  }
</script>

<style scoped>

</style>
