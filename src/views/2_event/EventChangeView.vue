<template>
  <div>
    <select name="" id="" @change="changeCity" v-model="selectedCity">
      <option value="">도시 선택</option>
      <option
        :value="city.cityCode"
        :key="city.cityCode"
        v-for="city in cityList"
      >
        {{ city.title }}
      </option>
    </select>
    <select name="" id="" v-model="selectedDong">
      <option
        :value="dong.dongCode"
        :key="dong.dongCode"
        v-for="dong in selectedDonglist"
      >
        {{ dong.dongTitle }}
      </option>
    </select>
    <br />
    {{ selectedCity }}
    <br />
    {{ selectedDong }}
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      selectedCity: "",
      selectedDong: "",
      cityList: [
        { cityCode: "02", title: "서울" },
        { cityCode: "03", title: "부산" },
        { cityCode: "04", title: "제주" },
      ],
      dongList: [
        { cityCode: "02", dongCode: "1", dongTitle: "서울1동" },
        { cityCode: "02", dongCode: "2", dongTitle: "서울2동" },
        { cityCode: "02", dongCode: "3", dongTitle: "서울3동" },
        { cityCode: "03", dongCode: "1", dongTitle: "부산1동" },
        { cityCode: "03", dongCode: "2", dongTitle: "부산2동" },
        { cityCode: "03", dongCode: "3", dongTitle: "부산3동" },
        { cityCode: "04", dongCode: "1", dongTitle: "제주1동" },
        { cityCode: "04", dongCode: "2", dongTitle: "제주" },
        { cityCode: "04", dongCode: "3", dongTitle: "제주3동" },
      ],
      selectedDonglist: [],
    }
  },
  methods: {
    changeCity() {
      this.selectedDonglist = this.dongList.filter(
        (dong) => dong.cityCode === this.selectedCity
      )
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
