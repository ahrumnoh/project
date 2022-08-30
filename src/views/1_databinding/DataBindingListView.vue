<!-- eslint-disable vue/valid-template-root -->
<template>
    <div>
        <div>
            <select name="" id="">
                <option value=""></option>
                <option :value="city.code" :key="city.code" v-for="city in cities">{{ city.title }}</option>

            </select>
        </div>
        <div>
            <table>
                <thead>
                    <tr>
                        <th>product number</th>
                        <th>product name</th>
                        <th>product price</th>
                        <th>product order qty</th>
                        <th>product sum</th>
                    </tr>
                </thead>
                <tbody>
                    <tr :key="drink.drinkId" v-for="drink in drinkList">
                        <td>{{drink.drinkId}}</td>
                        <td>{{drink.drinkName}}</td>
                        <td>{{drink.price}}</td>
                        <td><input type="number" name="" id="" v-model="drink.qty"></td>
                        <td>{{drink.price * drink.qty}}</td>
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
        { title: 'seoul', code: '02' },
        { title: 'gyungido', code: '031' },
        { title: 'jeju', code: '064' }
      ],
      drinkList: [
        {
          drinkId: '1',
          drinkName: 'coke',
          price: 200,
          qty: 1
        },
        {
          drinkId: '2',
          drinkName: 'juice',
          price: 150,
          qty: 1
        },
        {
          drinkId: '3',
          drinkName: 'milk',
          price: 300,
          qty: 1
        },
        {
          drinkId: '4',
          drinkName: 'grape juice',
          price: 80,
          qty: 1
        },
        {
          drinkId: '5',
          drinkName: 'strawberry juice',
          price: 120,
          qty: 1
        },
        {
          drinkId: '6',
          drinkName: 'mango juice',
          price: 110,
          qty: 1
        }
      ]
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>

<style scoped>

</style>
