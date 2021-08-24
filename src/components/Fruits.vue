<script>
export default {
  data() {
    return {
      fruits: [
        'Apple', 'Banana',' Cherry'
      ]
    }
  },
  computed: {
    hasFruit() {
      return this.fruits.length > 0
    },
    reverseFruits() {
      return this.fruits.map(fruit => {
        // 'Apple'.split => ['A','p','p','l','e'].reverse
        // => ['e','l','p','p','A'].join => 'elppA'
        return fruit.split('').reverse().join('')
      })
    }
  }
}
</script>

<template>
  <section v-if="hasFruit">
    <h1>Fruits</h1>
    <ul>
      <li
        v-for="fruit in fruits"
        :key="fruit">
        {{ fruit }}
      </li>
    </ul>
  </section>
  <br />
  <section v-if="reverseFruits">
    <h1>Reverse Fruits</h1>
    <ul>
      <li
        v-for="fruit in reverseFruits"
        :key="fruit">
        {{ fruit }}
      </li>
    </ul>
  </section>
</template>

<style lang="scss" scoped>
  h1 {
    color: forestgreen !important; //임포턴트 사용시 이후 타조건으로 재정의 안됨
    font-size: 30px;
  }
</style>