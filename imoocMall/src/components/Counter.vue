<template>
  <div>
    <button @click="increment">+</button>
    <button @click="decrement">-</button>
    <p>{{num}}</p>
  </div>
</template>

<script>
  export default {
    props: ["num"],
    name: "counter",
    data() {
      return {
        // num: 0
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
