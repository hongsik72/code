<template>
  <div>
    <div :style="style1">스타일 바인딩: 글씨는 레드</div>
    <button @click="style1.color = 'blue'">버튼</button>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      style1: {
        color: "red",
        fontSize: "30px",
      },
    }
  },
  methods: {},
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
