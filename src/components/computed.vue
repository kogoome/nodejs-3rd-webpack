<template>
  <h1>Computed</h1>
  <button @click="add">
    ADD
  </button>
  <br />
  msg: {{ msg }} <br />
  reversedMsg : {{ reversedMsg }}
</template>

<script>
export default {
  data() {
    return {
      //Getter Setter
      msg:'Hello Computed'
    }
  },
  computed: {
    //Getter
    reversedMsg() {
      return this.msg.split('').reverse().join('')
    },
    //Getter Setter
    reversedMessage: {
      get() {
        return this.msg.split('').reverse().join('')
      },
      set(value) {
        this.msg = value
      }
    }
  },
  methods: {
    add() {
      //this.reversedMsg += '!' 작동불
      this.msg += '!'
    }
  }
}
</script>

<style scoped lang="scss">
  h1{
    color: forestgreen;
    font-size: 50px;
  }
</style>