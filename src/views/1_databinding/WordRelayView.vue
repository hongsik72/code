<template>
  <div>
    <div>{{ word }}</div>
    <form v-on:submit="onSubmitForm">
      <input type="text" v-model="value" ref="answer" />
      <button type="submit">입력</button>
    </form>
    <div>{{ result }}</div>
  </div>
</template>
<script>
export default {
  name: "HelloWorld",

  data() {
    return {
      word: "제로초00",
      value: "",
      result: "",
    }
  },
  methods: {
    onSubmitForm(e) {
      e.preventDefault()
      if (this.word[this.word.length - 1] === this.value[0]) {
        this.result = "정답"
        this.word = this.value
        this.$refs.answer.focus()
        this.value = ""
      } else {
        this.result = "땡"
        this.$refs.answer.focus()
      }
    },
  },
}
</script>
