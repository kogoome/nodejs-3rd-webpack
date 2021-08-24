<template>
  <br />
  <Fruit />
  <br />
  <Computed />
  <br /><br />
  <Watch />
  <br /><br />
  <ComputedGetSet />
  <br /><br />
  <IsActive />
</template>

<script>
import Fruit from '~/components/Fruits'
import Computed from '~/components/computed'
import Watch from '~/components/watch'
import ComputedGetSet from "~/components/ComputedGetSet";
import IsActive from '~/components/isActive'

export default {
  components: {
    Fruit, Computed, Watch, ComputedGetSet, IsActive
  },
  data() {
    return {
    }
  },
}
</script>
