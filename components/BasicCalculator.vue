<template>
  <div class="basic-calc">
    <input type="number" v-model="numberOne" :style="`font-size: 22px; padding: ${calculatePadding(20)}px;`">
    <input type="number" v-model="numberTwo" :style="`font-size: 22px; padding: ${sumOfTwo}px;`">
    <!-- <button @click="calcSum">Calculate</button> -->
    <h3>Sum is: {{sumOfTwo}}</h3>
  </div>
</template>

<script>
export default {
  // mainīgās vertības, bet definētas iekšā katrā komponentē vienādi
  data () {
    return {
      numberOne: 0,
      numberTwo: 0
      // sumOfTwoManual: 0
    }
  },
  // mainīgās vērtības, kuras tiek definētas ārpus komponentes, jeb tad kad tā tiek izsaukta
  // piem: <BasicCaluculator :someProp="someValue"></BasicCaluculator>
  props: {

  },
  // izsaucās tad kad tiek izsaukta
  methods: {
    // variants ar pogu
    // calcSum () {
    //   this.sumOfTwoManual = parseInt(this.numberOne) + parseInt(this.numberTwo)
    // },
    calculatePadding (extraPadding) {
      return 22 + extraPadding
    }
  },
  // izcsaucās tajā brīdī kad pamainās kāda no izmantotajām vērtībām
  computed: {
    sumOfTwo () {
      return parseInt(this.numberOne) + parseInt(this.numberTwo)
    }
  }
}
</script>
