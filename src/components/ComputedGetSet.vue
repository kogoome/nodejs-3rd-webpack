<template>
  <h1 @click="add">
    {{ splitMsg }}
  </h1>
</template>

<script>
export default {
  name: "ComputedGetSet",
  data() {
    return {
      msg: 'ComputedMessage'
    }
  },
  computed: {
    splitMsg: {
      get() {
        return this.msg.split('').reverse().join('')
      },
      set(value) {
        this.msg = value
      }
    }
  },
  methods: {
    add(){
      this.splitMsg += '!'
    }
  }
}
</script>

<style scoped lang="scss">
  h1 {
    color: yellowgreen;
    font-size: 50px;
  }

</style>