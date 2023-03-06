<template>
  <div>
    <div>{{ first }}곱하기 {{ second }}는 </div>
    <form v-on:submit="onSubmitForm">
      <input type="number" v-model="value" ref="answer">
      <button type="submit">입력</button>
    </form>
    <div id="result">{{ result }}</div>
  </div>
</template>
<script>

export default {
  name: 'HelloWorld',
  data () {
    return {
      first: Math.ceil(Math.random() * 9),
      second: Math.ceil(Math.random() * 9),
      value: '',
      result: ''
    }
  },
  methods: {
    onSubmitForm(e) {
      e.preventDefault()
      console.log('first=' + this.first)
      console.log('second=' + this.second)
      if (this.first * this.second === this.value) {
        this.result = '정답'
        this.first = Math.ceil(Math.random() * 9)
        this.second = Math.ceil(Math.random() * 9)
        this.value = ''
        this.$refs.answer.focus()
      } else {
        this.result = '땡'
        this.$refs.answer.focus()
      }
    }
  }
}
</script>
