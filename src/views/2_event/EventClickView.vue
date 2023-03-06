<template>
  <div>
    <button @click="increaseCounter">Add 1</button>
    {{ counter }}
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      counter: 0,
    }
  },
  methods: {
    increaseCounter() {
      this.counter += 1
    },
  },
}
</script>
<style scoped>
.active {
  background-color: greenyellow;
  font-weight: bold;
}

.text-red {
  color: red;
}
</style>
