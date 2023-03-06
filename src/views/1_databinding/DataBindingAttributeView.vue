<template>
  <div>
    <input type="text" name="" id="" v-bind:value="userId" readonly />
    <br />
    <img :src="imgSrc" alt="" style="width: 200px; height: auto" />
    <br />
    <input type="search" name="" id="" v-model="txt1" />
    <button :disabled="txt1 === ''">조회</button>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      userId: "hongsik",
      imgSrc:
        "https://img4.daumcdn.net/thumb/R658x0.q70/?fname=https://t1.daumcdn.net/news/202301/08/mk/20230108200601433fmga.jpg",
      txt1: "",
    }
  },
}
</script>
