<template>
  <div>
    <button @click="disconnect" v-if="status === 'connected'">연결끊기</button>
    {{ message }}
    {{ message2 }}
  </div>
</template>
<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      message: "upload11",
      message2: "upload11",
    }
  },
  created() {
    let news = [
      {
        title: "kbs",
        newsList: "날씨1, 정치1, 경제1",
      },
      {
        title: "mbc",
        newsList: "날씨2, 정치2, 경제2",
      },
    ]

    function getNewsList([, { newsList }]) {
      console.log("newsList----", newsList)
    }

    getNewsList(news)

    //this.message2 = r
  },
  methods: {},
}
</script>
