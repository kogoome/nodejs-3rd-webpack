<template>
  <h1
    :class="{active:isActive}"
    @click="activate">
    isActive ({{ isActive }})
  </h1>
</template>

<script>
export default {
  name: "IsActive",
  data() {
    return {
      isActive: false
    }
  },
  methods: {
    activate() {
      this.isActive = !this.isActive
    }
  }
}
</script>

<style scoped>
.active {
  color: red;
}
</style>