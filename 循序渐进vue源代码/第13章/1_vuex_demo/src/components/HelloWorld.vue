<!-- <template>
  <h1>计数器{{ count }}</h1>
  <button @click="increment">增加</button>
</template>
<script>
export default {
  data() {
    return {
      count:0
    }
  },
  methods: {
    increment() {
      this.count ++
    }
  }
}
</script> -->

<template>
  <h1>计数器1:{{ this.$store.getters.countText }}</h1>
  <button @click="increment">增加</button>
</template>
<script>
export default {
  methods: {
    increment() {
      this.$store.commit('increment')
    }
  }
}
</script>