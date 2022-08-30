<!-- eslint-disable vue/valid-template-root -->
<template>
    <div>
        <select name="" id="" @change="changeCity" v-model="selectedCity">
        <!-- <select name="" id="" v-on:change="changeCity" v-model="selectedCity"> : the same function as above-->
            <option value=""> 📌 Select Cities</option>
            <option :value="city.cityCode" :key="city.cityCode" v-for="city in cityList"> {{ city.title }} </option>
        </select>
        <select name="" id="">
            <option :value="dong.dongCode" :key="dong.dongCode" v-for="dong in selectedDongList"> {{ dong.dongTitle }}</option>
        </select>
        <select name="" id="">
            <option :value="dong.dongCode" :key="dong.dongCode" v-for="dong in dongList.filter((dong) => dong.cityCode === selectedCity)"> {{ dong.dongTitle }}</option>
        </select>

    </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      selectedCity: '',
      cityList: [
        { cityCode: '02', title: 'seoul' },
        { cityCode: '031', title: 'gyungi' },
        { cityCode: '051', title: 'busan' },
        { cityCode: '064', title: 'jeju' }
      ],
      dongList: [
        { cityCode: '02', dongCode: '1', dongTitle: 'seoul-1dong' },
        { cityCode: '02', dongCode: '2', dongTitle: 'seoul-2dong' },
        { cityCode: '02', dongCode: '3', dongTitle: 'seoul-3dong' },
        { cityCode: '02', dongCode: '4', dongTitle: 'seoul-4dong' },
        { cityCode: '031', dongCode: '1', dongTitle: 'gyungi-1dong' },
        { cityCode: '031', dongCode: '2', dongTitle: 'gyungi-2dong' },
        { cityCode: '031', dongCode: '3', dongTitle: 'gyungi-3dong' },
        { cityCode: '031', dongCode: '4', dongTitle: 'gyungi-4dong' },
        { cityCode: '051', dongCode: '1', dongTitle: 'busan-1dong' },
        { cityCode: '051', dongCode: '2', dongTitle: 'busan-2dong' },
        { cityCode: '051', dongCode: '3', dongTitle: 'busan-3dong' },
        { cityCode: '051', dongCode: '4', dongTitle: 'busan-4dong' },
        { cityCode: '064', dongCode: '1', dongTitle: 'jeju-1dong' },
        { cityCode: '064', dongCode: '2', dongTitle: 'jeju-2dong' },
        { cityCode: '064', dongCode: '3', dongTitle: 'jeju-3dong' },
        { cityCode: '064', dongCode: '4', dongTitle: 'jeju-4dong' }
      ],
      selectedDongList: []
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {
    changeCity() {
      this.selectedDongList = this.dongList.filter((dong) => dong.cityCode === this.selectedCity)
    }
  }
}
</script>
