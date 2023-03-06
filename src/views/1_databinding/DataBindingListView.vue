<template>
  <div>
    <div>
      <select name="" id="">
        <option value="">선택하세요</option>
        <option value="city.code" :key="city.code" v-for="city in cities">
          {{ city.title }}
        </option>
      </select>
    </div>
    <br />
    <div>
      <table>
        <thead>
          <th>제품번호</th>
          <th>제품명</th>
          <th>가격</th>
          <th>수량</th>
          <th>합계</th>
        </thead>
        <tbody>
          <tr :key="drink.drinkId" v-for="drink in drinkList">
            <td>{{ drink.drinkId }}</td>
            <td>{{ drink.drinkName }}</td>
            <td>{{ drink.price }}</td>
            <td><input type="number" name="" id="" v-model="drink.qty" /></td>
            <td>{{ drink.price * drink.qty }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      cities: [
        { title: "서울", code: "02" },
        { title: "부산", code: "051" },
        { title: "제주", code: "064" },
      ],
      drinkList: [
        {
          drinkId: "1",
          drinkName: "콜라",
          price: 2600,
          qty: 10,
        },
        {
          drinkId: "2",
          drinkName: "우유",
          price: 1600,
          qty: 13,
        },
        {
          drinkId: "3",
          drinkName: "커피",
          price: 4300,
          qty: 13,
        },
        {
          drinkId: "4",
          drinkName: "쥬스",
          price: 2000,
          qty: 9,
        },
      ],
    }
  },
}
</script>
