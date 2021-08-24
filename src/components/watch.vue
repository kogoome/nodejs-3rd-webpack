<template>
  <h1 @click="addmsg">
    watch
  </h1>
  {{ msg }}
</template>

<script>
export default {
  name: "Watch",
  data() {
    return {
      msg: 'Hello World'
    }
  },
  methods: {
    addmsg() {
      this.msg += '!'
    }
  },
  watch: {
    msg() {
      console.log(this.msg)
    }
  }
}
</script>

<style scoped lang="scss">
h1{
  color: yellowgreen;
  font-size: 50px;
}
</style>